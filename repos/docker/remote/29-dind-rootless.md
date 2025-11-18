## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:e6ba97c94ca25ab093d673574223631a8d6548bddd274a91a28508e63857e8fb
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
$ docker pull docker@sha256:ea7d929ad6459e16db66e36da31b15949ab699c0e1ec88b8e21044a482fd563d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155077060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3838eb9febaeba29599f2046f223010db2b0f078d60340671720c036ff22b0b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 00:11:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 18 Nov 2025 00:11:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 18 Nov 2025 00:11:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 18 Nov 2025 00:11:13 GMT
ENV DOCKER_VERSION=29.0.2
# Tue, 18 Nov 2025 00:11:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 18 Nov 2025 00:11:13 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 18 Nov 2025 00:11:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 18 Nov 2025 00:11:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 18 Nov 2025 00:11:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 18 Nov 2025 00:11:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 18 Nov 2025 00:11:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:11:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 18 Nov 2025 00:11:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 18 Nov 2025 00:11:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:11:15 GMT
CMD ["sh"]
# Tue, 18 Nov 2025 00:18:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 18 Nov 2025 00:18:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 18 Nov 2025 00:18:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 18 Nov 2025 00:18:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 18 Nov 2025 00:18:18 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 18 Nov 2025 00:18:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 18 Nov 2025 00:18:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:18:18 GMT
VOLUME [/var/lib/docker]
# Tue, 18 Nov 2025 00:18:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 18 Nov 2025 00:18:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 18 Nov 2025 00:18:18 GMT
CMD []
# Tue, 18 Nov 2025 00:43:28 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 18 Nov 2025 00:43:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 18 Nov 2025 00:43:29 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 18 Nov 2025 00:43:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 18 Nov 2025 00:43:30 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 18 Nov 2025 00:43:30 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 18 Nov 2025 00:43:30 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa36a19b6f309c5ccbba1f5641401d233149c17e4edb23a3229b163961e0952d`  
		Last Modified: Tue, 18 Nov 2025 00:11:30 GMT  
		Size: 8.3 MB (8257277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ad8c4d68a0b3d10a7434d1b9cc5baa39b3dc551a5debe07ba47d2c3e4d2b21`  
		Last Modified: Tue, 18 Nov 2025 00:11:29 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adb7f0a335e8932b7af840cf6d13e8de76c174345515a60b77c41d4ef1df12d`  
		Last Modified: Tue, 18 Nov 2025 00:11:32 GMT  
		Size: 17.3 MB (17325954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adc1fd3f29e00ed27da9db9e4d33d519aefdbe1f598d10110eede759ab4ae56`  
		Last Modified: Tue, 18 Nov 2025 00:11:32 GMT  
		Size: 20.6 MB (20645060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b64c8b799bd25153f62a9c8518abfa930342788a9db84da6317167cc060ea1c`  
		Last Modified: Tue, 18 Nov 2025 00:11:32 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d70b150d1b09045eca8ed8881fd426ea62dde1ae536d8ed95260e1eee73263`  
		Last Modified: Tue, 18 Nov 2025 00:11:30 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f303d3a1595ad3940358a0eb25d247cd7635db2fd8405627a8a1ffee5046bb`  
		Last Modified: Tue, 18 Nov 2025 00:11:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1dc3018dfff03b5c7016e6ab5721b7d72caeddce1901f566eb08d9944ba420`  
		Last Modified: Tue, 18 Nov 2025 00:11:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8243179c7f9ac55fe223e9f2cb4bc8bc6d570e55d30506927ec1ef82bc9e143a`  
		Last Modified: Tue, 18 Nov 2025 00:18:38 GMT  
		Size: 7.1 MB (7140903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd952d6961543e7d762f05db654b734cd23d62bc5223ffcf8497b50465f8989`  
		Last Modified: Tue, 18 Nov 2025 00:18:37 GMT  
		Size: 99.5 KB (99500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61077e1cd8df73d90cbbbbc5cc3a14133f276b67b7283411f373d3d7af3d7897`  
		Last Modified: Tue, 18 Nov 2025 00:18:37 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c6ed8f9e4c26b54353f2de449036ee8325757494a7a1520d2b488a62973f40`  
		Last Modified: Tue, 18 Nov 2025 00:18:43 GMT  
		Size: 56.5 MB (56493955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0792056cc399838883ebc26c7485f97b307d92fdd813cf9982cae16ac4ba46d5`  
		Last Modified: Tue, 18 Nov 2025 00:18:37 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d989264b6b2b96cdd604c2244d01d2e2826c7bbda2db6c9b922a99eb1f37bdb5`  
		Last Modified: Tue, 18 Nov 2025 00:18:38 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117cb546a360d29ed2feed5ef01ff54e3816de8f8eb3401fb6dae3d57b49d4f4`  
		Last Modified: Tue, 18 Nov 2025 00:44:11 GMT  
		Size: 3.4 MB (3389939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4989a6e60f51e2504e878ed3c5063343c503cf99c0ca26ee99822b206ca3fe87`  
		Last Modified: Tue, 18 Nov 2025 00:44:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c018dbb8cd2f3cf8086c66d65504f44119dc99813baf70897731cae72a2cf3e`  
		Last Modified: Tue, 18 Nov 2025 00:44:11 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8094f2143a515ded89bc62d0a422b028f9adb52aa3bbe2ad65e92efbf3b8d432`  
		Last Modified: Tue, 18 Nov 2025 00:44:13 GMT  
		Size: 17.7 MB (17707042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e55bd6069b9e8264dbf5f93c02a2681ce7351618a3d8e524ad0842b46dbb90`  
		Last Modified: Tue, 18 Nov 2025 00:44:11 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:923b3c2215bc89330cd41d5436d03fcc87f40ce9b2d9ac0195e347bd813b1e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9dbf70f71b43121fa8994400db11122b48edfe88724ba54f95bc5551c9802f`

```dockerfile
```

-	Layers:
	-	`sha256:0012bd02e56638d2547abe3ef704b71f9c472541c326d18379f5fd85c51ddbba`  
		Last Modified: Tue, 18 Nov 2025 03:10:17 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:9fa64cfba4ca3ce1ce9b9bff37d132dcca40c57ca5572dd4b088b0ef96dd5d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:77b0d6c1d70145df2a845f6a4e93c0d575ef62913ff04621f19f439e37b5b2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161941003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f688acea7880189eb68325d9058adcdf18f1de639cbd78cd8676aa1179102264`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:32:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 08 May 2026 16:32:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 08 May 2026 16:32:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 08 May 2026 16:32:42 GMT
ENV DOCKER_VERSION=29.4.3
# Fri, 08 May 2026 16:32:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 08 May 2026 16:32:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 08 May 2026 16:32:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 08 May 2026 16:32:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 08 May 2026 16:32:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 08 May 2026 16:32:44 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 08 May 2026 16:32:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:32:44 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 08 May 2026 16:32:44 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 08 May 2026 16:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 16:32:44 GMT
CMD ["sh"]
# Fri, 08 May 2026 16:41:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 08 May 2026 16:41:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 08 May 2026 16:41:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 08 May 2026 16:41:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 08 May 2026 16:41:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 08 May 2026 16:41:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 08 May 2026 16:41:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:41:42 GMT
VOLUME [/var/lib/docker]
# Fri, 08 May 2026 16:41:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 08 May 2026 16:41:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 08 May 2026 16:41:42 GMT
CMD []
# Fri, 08 May 2026 17:11:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 08 May 2026 17:11:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 08 May 2026 17:11:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 08 May 2026 17:11:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 08 May 2026 17:11:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 08 May 2026 17:11:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 08 May 2026 17:11:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec23f98706aac7e78b99c5b57b1d75dec972dc79e3cacb916008f5d259aca1b`  
		Last Modified: Fri, 08 May 2026 16:32:50 GMT  
		Size: 8.4 MB (8390731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7913368a8c343e6c02c1adc847d8ec4459c10ca74d84a02703534599755e9f`  
		Last Modified: Fri, 08 May 2026 16:32:50 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a39f9ce9fa01d9f5397b1525f5e98a4d194e5ed65e85975d9b53425850f8009`  
		Last Modified: Fri, 08 May 2026 16:32:51 GMT  
		Size: 19.5 MB (19509764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdeda4e8c23988183983267fb1d9a88bb98e57eea25cd560e115091e0948d6c`  
		Last Modified: Fri, 08 May 2026 16:32:51 GMT  
		Size: 22.5 MB (22539224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1ff822b384d96d4595f7602097dec335b2acd5bc7676a8b940eafb0e1a7113`  
		Last Modified: Fri, 08 May 2026 16:32:52 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8578dbbf77b05f05c350ab61478118d90b33c33902ad5163a6eab6c9683129`  
		Last Modified: Fri, 08 May 2026 16:32:52 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67445366368bdf201719c21a984723732a1db81a14b254b1892415df7615ec5`  
		Last Modified: Fri, 08 May 2026 16:32:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee432c7809941439a94004d27e82a570ef307a339bb98d5b95170c5f41836e4`  
		Last Modified: Fri, 08 May 2026 16:32:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a671c8359481af8a9dd5758d4e04ef1d45ccdb46116d4091aed3a4b9bc07ab`  
		Last Modified: Fri, 08 May 2026 16:41:53 GMT  
		Size: 6.9 MB (6941745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee0895006e0fe072f423f3c654704551ae9a7fa1cba816c956a270b5e2ff8f1`  
		Last Modified: Fri, 08 May 2026 16:41:52 GMT  
		Size: 92.4 KB (92385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7749f84be70ca333897ee30d8e9fe5aadac34f53129c7c2e8c07585c05a7d1c6`  
		Last Modified: Fri, 08 May 2026 16:41:53 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7810bb43c760ae9fb8532068ce76928e893e014d57dc8691b07465f1376c41`  
		Last Modified: Fri, 08 May 2026 16:41:55 GMT  
		Size: 68.3 MB (68348863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918b28fa534e255a9d4127f8e25d21933682de41f27fed1f1b7556af42e0d41b`  
		Last Modified: Fri, 08 May 2026 16:41:54 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ccd0e7fb6611ab0a6b7198bc471eb620d601acfb4a1e03e4e6fddb6e916cd4`  
		Last Modified: Fri, 08 May 2026 16:41:54 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991fa3d3435205ac956f48c6cfde7edc5b29d5e5fa8b5e32b5ff1d39d937d9cb`  
		Last Modified: Fri, 08 May 2026 17:11:24 GMT  
		Size: 3.4 MB (3420143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b2ba9d9535d7ca362faea9d38d2b7f1d1b12ae4e454e6901ac9eb9a157716`  
		Last Modified: Fri, 08 May 2026 17:11:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3818d6139f86d609821f36157459df5eecce78adb118888d9b2474146bc2717`  
		Last Modified: Fri, 08 May 2026 17:11:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f240a9d758c24c96f87cab27d79880016cac9e61cc4de3b88024c9e836709f2`  
		Last Modified: Fri, 08 May 2026 17:11:24 GMT  
		Size: 17.6 MB (17580717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f5cbb09e55a4065b2862d9907bef876f7a27155424fd2796320ddabe11eb1f`  
		Last Modified: Fri, 08 May 2026 17:11:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:da8a6d0beba8917b4e52857d269469a972215ede87884f429cebcb8b0bf6c3a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49ced8ac9f99a66c4082c87a6e3700965441b6d3dbd682c649c874129465e94`

```dockerfile
```

-	Layers:
	-	`sha256:da8459f5ac1514cf7a308371bfa80dd5ac7dc5e580d0e698f9412fe2634cd8cf`  
		Last Modified: Fri, 08 May 2026 17:11:23 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6e504d0b8002c8ff4311bd0a4ad09efc48b3e1115211c3be472253705f73d011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151776962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ad245e6cb1bc4f621a876a658b480aa2b21af7ded62d996d0b804a0c5b6626`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:30:58 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 08 May 2026 16:30:58 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 08 May 2026 16:30:58 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 08 May 2026 16:31:00 GMT
ENV DOCKER_VERSION=29.4.3
# Fri, 08 May 2026 16:31:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 08 May 2026 16:31:00 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 08 May 2026 16:31:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 08 May 2026 16:31:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Fri, 08 May 2026 16:31:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 08 May 2026 16:31:02 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 08 May 2026 16:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:31:02 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 08 May 2026 16:31:02 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 08 May 2026 16:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 16:31:02 GMT
CMD ["sh"]
# Fri, 08 May 2026 16:37:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 08 May 2026 16:37:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 08 May 2026 16:37:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 08 May 2026 16:37:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 08 May 2026 16:37:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 08 May 2026 16:37:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 08 May 2026 16:37:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:37:42 GMT
VOLUME [/var/lib/docker]
# Fri, 08 May 2026 16:37:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 08 May 2026 16:37:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 08 May 2026 16:37:42 GMT
CMD []
# Fri, 08 May 2026 17:11:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 08 May 2026 17:11:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 08 May 2026 17:11:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 08 May 2026 17:11:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 08 May 2026 17:11:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 08 May 2026 17:11:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 08 May 2026 17:11:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16557002e3f9c0f12daad3cf2aa0eeb951785238e78f649fe1a33be164ee3cd`  
		Last Modified: Fri, 08 May 2026 16:31:08 GMT  
		Size: 8.5 MB (8450503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba2f25b8074cba3c42ab763faf8c1eec97f0f1268e18221c315fd39a71cfbc`  
		Last Modified: Fri, 08 May 2026 16:31:07 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd0d50d3cbd05ec2ff1d935bcb728e2c0906b010fa46bec38094653add3d6fa`  
		Last Modified: Fri, 08 May 2026 16:31:08 GMT  
		Size: 18.0 MB (17969147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d520c49f69c93efe2c8a5a65659a79b0627ebde2251cc670896e5ee2fbbf9bb`  
		Last Modified: Fri, 08 May 2026 16:31:08 GMT  
		Size: 20.5 MB (20453109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873efcc71ab19d6817bcd802ce087ef621ee9d76ef00ccba44a47ea3b2312b2`  
		Last Modified: Fri, 08 May 2026 16:31:09 GMT  
		Size: 10.2 MB (10243273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11571ea79227e8cd2b7926c36cd8148f1a6566edd6cab24a2f56b91ea6534a3`  
		Last Modified: Fri, 08 May 2026 16:31:09 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a0b06ba0679ee8b78ca3c2dd121c5e7e2dccb9e4ec1eb19c8e9522d1583b20`  
		Last Modified: Fri, 08 May 2026 16:31:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc867a92a4a00d8508b93d50da952ca51038d284ade22fd6e0589b2513306b79`  
		Last Modified: Fri, 08 May 2026 16:31:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d757bdfc2e9a45824a5bdda812b99f3be75676212405a806df980f32a42cbf9b`  
		Last Modified: Fri, 08 May 2026 16:37:51 GMT  
		Size: 7.2 MB (7219905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccad4339e14b0820bef18f0b258d4327d08194aad4210de1f10aaccef4a61093`  
		Last Modified: Fri, 08 May 2026 16:37:51 GMT  
		Size: 101.2 KB (101156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00443b9d7dd6076f7ffdddc1551fce7af349e3173b164e83d4bd48a9e773bc1d`  
		Last Modified: Fri, 08 May 2026 16:37:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f491a26ce184e2829f420ce2c7b629796cd7cee708354990994076452a8f34`  
		Last Modified: Fri, 08 May 2026 16:37:53 GMT  
		Size: 61.9 MB (61853059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11205509ebe2299412035c22ccd1a53f13aedf03fc556f02386ea9b89431e1b0`  
		Last Modified: Fri, 08 May 2026 16:37:52 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a75d4c1067c85b48d61a75ea8c37718511cc364047bb2e2288fa0dab3385d78`  
		Last Modified: Fri, 08 May 2026 16:37:52 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98a8345399e7e0b38f35a8fb6f5eb845564989f27397a122fb1e218fe50c44`  
		Last Modified: Fri, 08 May 2026 17:11:23 GMT  
		Size: 3.4 MB (3394545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c862d483c24147feab27716b7fb21e4e360bc1264f8269590bae71c9cb0cb72`  
		Last Modified: Fri, 08 May 2026 17:11:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4239627cd7145a2f13d79570e4036b6ca72d76a0c21b1cb299e704680226fa`  
		Last Modified: Fri, 08 May 2026 17:11:22 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f48835c96d625313d061225e1e95fb05eaaa27e095f528fb5f3f7ba73977e6`  
		Last Modified: Fri, 08 May 2026 17:11:23 GMT  
		Size: 17.9 MB (17882902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5e03f2d4d7102af4320af80bfecd72297ef2716aceaa1af61ef144c1f09655`  
		Last Modified: Fri, 08 May 2026 17:11:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:8066c28689c32095d4981a273e8eb9725b7d833509d7d2455ee1671f568ad813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3d91c30e63cb35d064dbdd65db95b7be1762200834b0497ab85a422474e5fb`

```dockerfile
```

-	Layers:
	-	`sha256:c9ccf1017fe481226414949a5e4201668292fd12608ecd7ec44d390ac0ebf1e2`  
		Last Modified: Fri, 08 May 2026 17:11:22 GMT  
		Size: 30.8 KB (30759 bytes)  
		MIME: application/vnd.in-toto+json

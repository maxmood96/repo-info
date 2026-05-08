<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.4`](#docker294)
-	[`docker:29.4-cli`](#docker294-cli)
-	[`docker:29.4-dind`](#docker294-dind)
-	[`docker:29.4-dind-rootless`](#docker294-dind-rootless)
-	[`docker:29.4-windowsservercore`](#docker294-windowsservercore)
-	[`docker:29.4-windowsservercore-ltsc2022`](#docker294-windowsservercore-ltsc2022)
-	[`docker:29.4-windowsservercore-ltsc2025`](#docker294-windowsservercore-ltsc2025)
-	[`docker:29.4.3`](#docker2943)
-	[`docker:29.4.3-alpine3.23`](#docker2943-alpine323)
-	[`docker:29.4.3-cli`](#docker2943-cli)
-	[`docker:29.4.3-cli-alpine3.23`](#docker2943-cli-alpine323)
-	[`docker:29.4.3-dind`](#docker2943-dind)
-	[`docker:29.4.3-dind-alpine3.23`](#docker2943-dind-alpine323)
-	[`docker:29.4.3-dind-rootless`](#docker2943-dind-rootless)
-	[`docker:29.4.3-windowsservercore`](#docker2943-windowsservercore)
-	[`docker:29.4.3-windowsservercore-ltsc2022`](#docker2943-windowsservercore-ltsc2022)
-	[`docker:29.4.3-windowsservercore-ltsc2025`](#docker2943-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:c77e5d7912f9b137cc67051fdc2991d8f5ae22c55ddf532bb836dcb693a04940
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
$ docker pull docker@sha256:df0a33cee340ca6bf54b991776aa7b0adecd2f11f426e91a855205c4dede6687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140938664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b402db1b520b21284360af908099d81330e3a0abfb470068d0b691394f830f8a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:59:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:59:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:59:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:59:36 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53c3ea41339525629cfebd67afd71158e26f974aa002b648300d6b51b0a7f0`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 6.9 MB (6941788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042a8c82cc770b77ff12697783c5d4f58f4a1158c393d8d7bf48c66938dd0364`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e52c67d04087c8634de6b8e00bea30bbbfb9f44b910535df2fcf39d218a76e`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642357ac7fa1a3a23ac6950bf37044c34f3e2baf0302453327f0f0f9c07b625`  
		Last Modified: Mon, 20 Apr 2026 23:59:48 GMT  
		Size: 68.3 MB (68349083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b558d88b0e2089a0084bc1ecf86456f88572debf4e7c409c5b6a9e6a4f1c9`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c3644d4203c234122b18a9c209f1d9346bdf3ae77c865f94bb5d413b0e3ed`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:f8e5ff02cd7ab58746eba767c8cfe72659ebf0cdbc5ad53966962f5be76bb240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afcdfebb2919edf2decaff61a49a454d38f00fb49947b2a11b30fe59307eb26`

```dockerfile
```

-	Layers:
	-	`sha256:4a3c63758eb59daa26239d0a9f489fbc493b5c9520a02ee9e025dbaf9beddfcf`  
		Last Modified: Mon, 20 Apr 2026 23:59:45 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:714765536f9b13db2b7aac00ba2108c2e72491db611b2507a2dceb9cedc34edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132889403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4457d3d11f719e5294f8d032dfa5fb5584b7bb429a3c771be010f3c301a17ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:02:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:02:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:02:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:02:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:02:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:02:41 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:53 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:53 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e3ffaa23a53656a701abccec699e0622634777630e64cc504cff3d98dea60`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 8.3 MB (8297071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d350fb58b43c87a2a610f7888a7e169fbede9d23cbbf95f2f4baf73bfd058`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e71abc6298cfba6b269fcfc40efb671d56bd1a064bc669fb2569f96b3d9e98`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 18.2 MB (18156872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e844e057391513e9df6248a894061b3da111c79353463cc9293756d4682ebb`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 21.2 MB (21151868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d685033686f50b3e8f899849b292620ebe6095b84b19804734c9bf296da664`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 10.7 MB (10650797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854d1c1455463deb73d9ab0f6d7c04ba88225a33b0abf99cad5ba5be3fa9747`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ac870adbf89552657dab35d34258189f063c92bbeed903264859d2d64f304`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9337155e0b0c7eac32aafb07f862d35bdb185109213953d1e6bbf0b1f11939`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e31ea6b8650fd1cb9e50ee87e2adeb53f639a46bc5637a30509b4f2199c7a6`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 7.3 MB (7278534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05a60dd7fb89408541e99b9add9de0a0ed0fc5e1284f41dabf1dc7759413a89`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 91.7 KB (91681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb9c2c8813a470d643b478d97ee7cc9276c03c191f89e5f089c9c8af175a405`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e43bc415892250863a3c4af768f7ce347c30f4833a6a1e4a67768b501440ab`  
		Last Modified: Mon, 20 Apr 2026 23:07:06 GMT  
		Size: 63.7 MB (63682576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d001b30e4e7638598e7d353011d5b96582f31c29966d81492d68be9dabd785e`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bc8f4ddf7c3ad344ffb154ed638043188cdf4538adf0f249190938fc860463`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:47917b39931d5ff122cad720bb4846feec49fd1a70b68d9e80e0d17ce3d053fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d7b0c669a63da8adb11eee50731ea3933b923b2d3b6b3225028584b477c489`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea91ea0ce644175b943604f88c7d3ba89c5639a0373b5723b1455c6e7dd69`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:9b5665d5b82efba3f0dc4f195e3ffaefe1836577d2b82087a17f661cbdba9e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130968276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1540fdf9c9f6e2b278b27f2d4b2fffee4d93dea59718690376088e013517a488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:03:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:03:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:03:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:03:08 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:25 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67eb8b211b126a9b196c63931bfb05d72f87744ae67d6192ad13cf450e7a546`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 7.6 MB (7595775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34795d272397574b7b3e5108ed44e92aba790269dcb1bb8857915901d01f3bb`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a502b029b4b1ca6ac391718dddbb8226630ff4608fa9ad06915082bf30527a3`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 18.1 MB (18140306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b761e09f613d3b9783119e6089286c6f1ecc317627f83a2db382367f9532a`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 21.1 MB (21129738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1f0057cba8c1b61b31a0083e2b2391654b4326c8cf941fb10cdcf5c594db26`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 10.6 MB (10637140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95270af0c20972fbc14c1290b3763d03c43ce137600ca407541a323d815ea47`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff9fae5081b926ea54eabe7f33064f939afc5dda9a9eb52efb73470050f4517`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de53539477ce329ea36134755ab02f30f3d649500c60b42843af353baa1c525`  
		Last Modified: Mon, 20 Apr 2026 23:03:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efb5f9a5a71a55f54b6b99486f1bd5c1ea083613d951c96d61aaaa17077efbc`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 6.6 MB (6577240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f089c2d980079da58da3c0bec29a2b33a46373b348c2d134c18dd2431ddc248`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 88.0 KB (88020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f8cdc4960364c34cd8577f5d1b471c13ff2da3690c99299165c1073d51400`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40e7e3397d39afd124ad68cc95b2562142ff2610fce88b9aac86632e51a84f1`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 63.5 MB (63508793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ded61da57df247bd913fc7aad237f90938281d803dc83cc68b45346172aaa`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057e69e7417d0aff4a580b1aaf265dc3047522821113d8d29c120c580b8dcdea`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:31adf82453b129c500c21266951d25762d0a1d8612c4d45b214ad2ec9cde0b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcdfa8f44b536121dca093b7db18543a07667c4eccb50fc1484ddc883d5acfe`

```dockerfile
```

-	Layers:
	-	`sha256:0060530a92e8a426030ba97ebb924869a17e6a5b29719b92b59163c260a3f2d0`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ee74da04f9e09444b1d5ef2a8dbe82c89528d8de11715101b40c14a09e2cf37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130498772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a186abf796a2c5525e161a14df33c5cee12bbe6164dff8f6419f97e74b8f420`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:58:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:58:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:58:42 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b102c50bc0bd848d63594177b3551f950afb81cf23769056498c471acef763a8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 7.2 MB (7219870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffadf95cb7de624b076a0d462fa3480612216001cb1bc1977a7f7c68dd492e`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c0362756805190c2877fb2ba65ac0d7335b212c601a891a40a869a2121d2a`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6689be7b2deb380b56446eca8f0ff2610db9e7a9e33ffe8e5ce8255459333b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 61.9 MB (61854105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c32c7cfcb98ead6efe658a6dede3f1c6de4b8f676102e76dbf7519fcb80cd6`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fedc2d525bb8a19fc39fdec7b591d4dd6cbcd58ecab8ef85f4a50244792ce0b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:e5381b0fdc4555ad09b2c07b4d9a15f173eb5a42322aa01332df83c945a0bee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c928de50165b5f7d2c8e4732d512b1762d46ba6b1367c0726deefca1a9b74a8`

```dockerfile
```

-	Layers:
	-	`sha256:b37182aafc731f3098dfc2cefd626d2996f42916d78a5c3efed84580685c1ad8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:17b5c235f40be7432a7c0914c154e9278aed63bad4afe5607e4f91840696a9f8
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
$ docker pull docker@sha256:ea475cbe5f579d671563e49753456303d706aa4eeaed57598aed5f976c252ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65549408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2596d6d85c20a8881389ccdca1db9b5bfdd2acbf2c9de29f2c5d68c5b7865e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8c678f6c52c4c82d7427fb6dddceeaeaf0fbc7a6450754f8d06fc88b89230084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a381a0af73b712a4aebbe9431b9ac9b119cf19ccab56ef9bc230d42208fe80`

```dockerfile
```

-	Layers:
	-	`sha256:9b00532c7328d5c1c13da3bb1a995e11d78eb22857649a7b2b898736c1b5d40a`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:1e75504955c5f006f5a647b25bebdd04958bcae39df9b5dc452f17d85f7cd892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61830622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87398cb4a53dd8a56381484fc5577e2ae102de114476ded1f78d7269bf33ada9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:02:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:02:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:02:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:02:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:02:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:02:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e3ffaa23a53656a701abccec699e0622634777630e64cc504cff3d98dea60`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 8.3 MB (8297071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d350fb58b43c87a2a610f7888a7e169fbede9d23cbbf95f2f4baf73bfd058`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e71abc6298cfba6b269fcfc40efb671d56bd1a064bc669fb2569f96b3d9e98`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 18.2 MB (18156872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e844e057391513e9df6248a894061b3da111c79353463cc9293756d4682ebb`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 21.2 MB (21151868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d685033686f50b3e8f899849b292620ebe6095b84b19804734c9bf296da664`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 10.7 MB (10650797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854d1c1455463deb73d9ab0f6d7c04ba88225a33b0abf99cad5ba5be3fa9747`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ac870adbf89552657dab35d34258189f063c92bbeed903264859d2d64f304`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9337155e0b0c7eac32aafb07f862d35bdb185109213953d1e6bbf0b1f11939`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:49bea12963a6abdd2981540b1f9f1d376ddf62a3b59bfa513300247bbc3362b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fc4edc3e7b36ff7db3bbbf4485b370c0140889b743ede632d7e904abb13280`

```dockerfile
```

-	Layers:
	-	`sha256:56e0cb7a74a706120b1715854bd1ca2075f69c6188b79bd76c37f0d35d344edb`  
		Last Modified: Mon, 20 Apr 2026 23:02:47 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b13f70e6887b08b891cda119e675ca58eae33277cc384f8c978046fa173d60a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60788235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fbaf5ba1970836d18097d7cf38e4cb04484bb6e501bee5d4106a2d77a2ff52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:03:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:03:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:03:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:03:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67eb8b211b126a9b196c63931bfb05d72f87744ae67d6192ad13cf450e7a546`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 7.6 MB (7595775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34795d272397574b7b3e5108ed44e92aba790269dcb1bb8857915901d01f3bb`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a502b029b4b1ca6ac391718dddbb8226630ff4608fa9ad06915082bf30527a3`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 18.1 MB (18140306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b761e09f613d3b9783119e6089286c6f1ecc317627f83a2db382367f9532a`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 21.1 MB (21129738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1f0057cba8c1b61b31a0083e2b2391654b4326c8cf941fb10cdcf5c594db26`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 10.6 MB (10637140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95270af0c20972fbc14c1290b3763d03c43ce137600ca407541a323d815ea47`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff9fae5081b926ea54eabe7f33064f939afc5dda9a9eb52efb73470050f4517`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de53539477ce329ea36134755ab02f30f3d649500c60b42843af353baa1c525`  
		Last Modified: Mon, 20 Apr 2026 23:03:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ae2e1d6be0d9232d64e8084bbb20b97bf932e41046e7ca77d8892c0d074a3220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2880778d01f572e158741e29a37b481691803371ae7ad079df2041fa43bd74e`

```dockerfile
```

-	Layers:
	-	`sha256:e1966d50533bdd80bf5331881d8e0ad7144144431fc76c6c5dfeb0fe82bb49ca`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:24b137d1441b41c4aa60cd5a38d069feb70e191d8c4340bcf9a7ad9b86aefb23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61317637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbbbbe92229c40c0c4fa922cff0ddafbd7d744d4652c3238ddbf132a70c1657`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3a941d5f19c61b4b5b16ad9371e7493c1548990d5cc7bddb7661c14e2572fba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e469bc2dde45b7974017a985c18538a4c3735c73f0e8c3e74cdc0e37d15f0a7a`

```dockerfile
```

-	Layers:
	-	`sha256:b845891250bf1a1824d4d301d2e389c000ebcc1e79af3839f42801d7e13f2ab5`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:c77e5d7912f9b137cc67051fdc2991d8f5ae22c55ddf532bb836dcb693a04940
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
$ docker pull docker@sha256:df0a33cee340ca6bf54b991776aa7b0adecd2f11f426e91a855205c4dede6687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140938664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b402db1b520b21284360af908099d81330e3a0abfb470068d0b691394f830f8a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:59:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:59:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:59:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:59:36 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53c3ea41339525629cfebd67afd71158e26f974aa002b648300d6b51b0a7f0`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 6.9 MB (6941788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042a8c82cc770b77ff12697783c5d4f58f4a1158c393d8d7bf48c66938dd0364`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e52c67d04087c8634de6b8e00bea30bbbfb9f44b910535df2fcf39d218a76e`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642357ac7fa1a3a23ac6950bf37044c34f3e2baf0302453327f0f0f9c07b625`  
		Last Modified: Mon, 20 Apr 2026 23:59:48 GMT  
		Size: 68.3 MB (68349083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b558d88b0e2089a0084bc1ecf86456f88572debf4e7c409c5b6a9e6a4f1c9`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c3644d4203c234122b18a9c209f1d9346bdf3ae77c865f94bb5d413b0e3ed`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f8e5ff02cd7ab58746eba767c8cfe72659ebf0cdbc5ad53966962f5be76bb240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afcdfebb2919edf2decaff61a49a454d38f00fb49947b2a11b30fe59307eb26`

```dockerfile
```

-	Layers:
	-	`sha256:4a3c63758eb59daa26239d0a9f489fbc493b5c9520a02ee9e025dbaf9beddfcf`  
		Last Modified: Mon, 20 Apr 2026 23:59:45 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:714765536f9b13db2b7aac00ba2108c2e72491db611b2507a2dceb9cedc34edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132889403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4457d3d11f719e5294f8d032dfa5fb5584b7bb429a3c771be010f3c301a17ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:02:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:02:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:02:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:02:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:02:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:02:41 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:53 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:53 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e3ffaa23a53656a701abccec699e0622634777630e64cc504cff3d98dea60`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 8.3 MB (8297071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d350fb58b43c87a2a610f7888a7e169fbede9d23cbbf95f2f4baf73bfd058`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e71abc6298cfba6b269fcfc40efb671d56bd1a064bc669fb2569f96b3d9e98`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 18.2 MB (18156872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e844e057391513e9df6248a894061b3da111c79353463cc9293756d4682ebb`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 21.2 MB (21151868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d685033686f50b3e8f899849b292620ebe6095b84b19804734c9bf296da664`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 10.7 MB (10650797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854d1c1455463deb73d9ab0f6d7c04ba88225a33b0abf99cad5ba5be3fa9747`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ac870adbf89552657dab35d34258189f063c92bbeed903264859d2d64f304`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9337155e0b0c7eac32aafb07f862d35bdb185109213953d1e6bbf0b1f11939`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e31ea6b8650fd1cb9e50ee87e2adeb53f639a46bc5637a30509b4f2199c7a6`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 7.3 MB (7278534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05a60dd7fb89408541e99b9add9de0a0ed0fc5e1284f41dabf1dc7759413a89`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 91.7 KB (91681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb9c2c8813a470d643b478d97ee7cc9276c03c191f89e5f089c9c8af175a405`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e43bc415892250863a3c4af768f7ce347c30f4833a6a1e4a67768b501440ab`  
		Last Modified: Mon, 20 Apr 2026 23:07:06 GMT  
		Size: 63.7 MB (63682576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d001b30e4e7638598e7d353011d5b96582f31c29966d81492d68be9dabd785e`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bc8f4ddf7c3ad344ffb154ed638043188cdf4538adf0f249190938fc860463`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:47917b39931d5ff122cad720bb4846feec49fd1a70b68d9e80e0d17ce3d053fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d7b0c669a63da8adb11eee50731ea3933b923b2d3b6b3225028584b477c489`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea91ea0ce644175b943604f88c7d3ba89c5639a0373b5723b1455c6e7dd69`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:9b5665d5b82efba3f0dc4f195e3ffaefe1836577d2b82087a17f661cbdba9e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130968276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1540fdf9c9f6e2b278b27f2d4b2fffee4d93dea59718690376088e013517a488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:03:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:03:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:03:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:03:08 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:25 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67eb8b211b126a9b196c63931bfb05d72f87744ae67d6192ad13cf450e7a546`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 7.6 MB (7595775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34795d272397574b7b3e5108ed44e92aba790269dcb1bb8857915901d01f3bb`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a502b029b4b1ca6ac391718dddbb8226630ff4608fa9ad06915082bf30527a3`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 18.1 MB (18140306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b761e09f613d3b9783119e6089286c6f1ecc317627f83a2db382367f9532a`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 21.1 MB (21129738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1f0057cba8c1b61b31a0083e2b2391654b4326c8cf941fb10cdcf5c594db26`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 10.6 MB (10637140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95270af0c20972fbc14c1290b3763d03c43ce137600ca407541a323d815ea47`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff9fae5081b926ea54eabe7f33064f939afc5dda9a9eb52efb73470050f4517`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de53539477ce329ea36134755ab02f30f3d649500c60b42843af353baa1c525`  
		Last Modified: Mon, 20 Apr 2026 23:03:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efb5f9a5a71a55f54b6b99486f1bd5c1ea083613d951c96d61aaaa17077efbc`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 6.6 MB (6577240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f089c2d980079da58da3c0bec29a2b33a46373b348c2d134c18dd2431ddc248`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 88.0 KB (88020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f8cdc4960364c34cd8577f5d1b471c13ff2da3690c99299165c1073d51400`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40e7e3397d39afd124ad68cc95b2562142ff2610fce88b9aac86632e51a84f1`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 63.5 MB (63508793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ded61da57df247bd913fc7aad237f90938281d803dc83cc68b45346172aaa`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057e69e7417d0aff4a580b1aaf265dc3047522821113d8d29c120c580b8dcdea`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:31adf82453b129c500c21266951d25762d0a1d8612c4d45b214ad2ec9cde0b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcdfa8f44b536121dca093b7db18543a07667c4eccb50fc1484ddc883d5acfe`

```dockerfile
```

-	Layers:
	-	`sha256:0060530a92e8a426030ba97ebb924869a17e6a5b29719b92b59163c260a3f2d0`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ee74da04f9e09444b1d5ef2a8dbe82c89528d8de11715101b40c14a09e2cf37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130498772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a186abf796a2c5525e161a14df33c5cee12bbe6164dff8f6419f97e74b8f420`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:58:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:58:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:58:42 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b102c50bc0bd848d63594177b3551f950afb81cf23769056498c471acef763a8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 7.2 MB (7219870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffadf95cb7de624b076a0d462fa3480612216001cb1bc1977a7f7c68dd492e`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c0362756805190c2877fb2ba65ac0d7335b212c601a891a40a869a2121d2a`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6689be7b2deb380b56446eca8f0ff2610db9e7a9e33ffe8e5ce8255459333b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 61.9 MB (61854105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c32c7cfcb98ead6efe658a6dede3f1c6de4b8f676102e76dbf7519fcb80cd6`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fedc2d525bb8a19fc39fdec7b591d4dd6cbcd58ecab8ef85f4a50244792ce0b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e5381b0fdc4555ad09b2c07b4d9a15f173eb5a42322aa01332df83c945a0bee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c928de50165b5f7d2c8e4732d512b1762d46ba6b1367c0726deefca1a9b74a8`

```dockerfile
```

-	Layers:
	-	`sha256:b37182aafc731f3098dfc2cefd626d2996f42916d78a5c3efed84580685c1ad8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:b195ea3784d101abfe1ac68a47f95bcde74bb7ea4e4e8d277d29bc2661a6ae0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:90ee5b76cb0ac744decd66b40bf8c28137072a5c057ec0ee1929ecdbb221d36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161940861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fabb463ad72abee35979cb5448a0a39f5913b0010186d096e512ca7b033451`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:59:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:59:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:59:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:59:36 GMT
CMD []
# Tue, 21 Apr 2026 00:08:21 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 21 Apr 2026 00:08:21 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 21 Apr 2026 00:08:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 21 Apr 2026 00:08:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 21 Apr 2026 00:08:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 21 Apr 2026 00:08:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 21 Apr 2026 00:08:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53c3ea41339525629cfebd67afd71158e26f974aa002b648300d6b51b0a7f0`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 6.9 MB (6941788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042a8c82cc770b77ff12697783c5d4f58f4a1158c393d8d7bf48c66938dd0364`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e52c67d04087c8634de6b8e00bea30bbbfb9f44b910535df2fcf39d218a76e`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642357ac7fa1a3a23ac6950bf37044c34f3e2baf0302453327f0f0f9c07b625`  
		Last Modified: Mon, 20 Apr 2026 23:59:48 GMT  
		Size: 68.3 MB (68349083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b558d88b0e2089a0084bc1ecf86456f88572debf4e7c409c5b6a9e6a4f1c9`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c3644d4203c234122b18a9c209f1d9346bdf3ae77c865f94bb5d413b0e3ed`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6326f615a955ae1eaedcfd9398e20d690369774c11792fa677315a2ee4edc0eb`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 3.4 MB (3420140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab423da3008515c1f53f14584a5eec29fd4872007b06158bf377fa09ba064a75`  
		Last Modified: Tue, 21 Apr 2026 00:08:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1226b4652a0375b13cf8982005f49f46b4ea918f3afdeb0631639fbbc3314b7d`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7972f6fab882aea0a0a19ba34beda49c3a1fbc3fa74c8f1623babc91d75d88`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 17.6 MB (17580715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74b8d79d9c7fe010571a301be54bec8ec1b4d7367bd0f213d1156fd0dc66b80`  
		Last Modified: Tue, 21 Apr 2026 00:08:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1df8001a7b67a92a6737daee6dd9872da616bc3739aeaa1373577cb29a570e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670d44ba2e33335446b40d2adf46f25e8eb9622108be15df50e4e534c8d509e`

```dockerfile
```

-	Layers:
	-	`sha256:a576e6e994270734040c0f9b4683c7148fce217d815f34c6ebd4513dfc2fb099`  
		Last Modified: Tue, 21 Apr 2026 00:08:28 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a8b05ad135b3c2aaf1cc2740342e7dced62e131746edba5716795edc6ab5fe0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151777543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f34433de1df012f3564979b68c8ecbea41a0994f744ffc1a0abc1ab348b4895`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:58:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:58:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:58:42 GMT
CMD []
# Tue, 21 Apr 2026 00:08:28 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 21 Apr 2026 00:08:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 21 Apr 2026 00:08:28 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 21 Apr 2026 00:08:30 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b102c50bc0bd848d63594177b3551f950afb81cf23769056498c471acef763a8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 7.2 MB (7219870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffadf95cb7de624b076a0d462fa3480612216001cb1bc1977a7f7c68dd492e`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c0362756805190c2877fb2ba65ac0d7335b212c601a891a40a869a2121d2a`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6689be7b2deb380b56446eca8f0ff2610db9e7a9e33ffe8e5ce8255459333b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 61.9 MB (61854105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c32c7cfcb98ead6efe658a6dede3f1c6de4b8f676102e76dbf7519fcb80cd6`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fedc2d525bb8a19fc39fdec7b591d4dd6cbcd58ecab8ef85f4a50244792ce0b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef5707b49ab3f9adf26a56a9cbf6e4e78517b050e3b2fb0364f0da00f24be43`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 3.4 MB (3394528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93e0c3f1bc24f5a906884d4f60c44e459576b94f446616a5d85b9f99099e64d`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac4a74a9a53d69bcedb3a35d02f3cd37a6d429742ab1fdb508f31d983f54d86`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97af490d1d2239d0247cd840d1484d5d454ca169df2085b09c458aafd6fd0b4`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 17.9 MB (17882904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89238103243275f2a60886defdafc2cc3273f86991b81361f68cb4412a1ce84`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f2fcd0a8c8910cfe23cdc7b7f806a4a6f2a4e768fe42fff95f3b6b4bf7fa251a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77b04e174c6dfe0ab7846a82c85075337e3469d0ef0167dae8c0290864c79eb`

```dockerfile
```

-	Layers:
	-	`sha256:1e998a2dfee9b2b9098be9e582d8f43b4229d3689201c39322666ffefa251c5e`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 30.8 KB (30759 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:5106320dcd9789d033f8f0201b14e4d4e4b03061f7826fbee5f04f1beef77315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:93470c750610123e91ad43f5b232a408d9ddd6f4bea2355e23cf1996338a8c6e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186012082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa0979c8bbd379ec0dbae2915024f4ffde2fac2bcc3ba3b496f98c9b7bd3619`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Mon, 20 Apr 2026 23:07:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:08:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:08:29 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:08:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:08:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:46 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:08:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:09:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdee3346b7a1b8ad53c9f8e5dd67903ff39beed2f224ac303b25f0dd869f8a8`  
		Last Modified: Mon, 20 Apr 2026 23:09:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa8f0463cf87863a82f8ca46c43dff6bfb2f9c87c13e93e06a6edd06c8b750`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 392.9 KB (392898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e18e138890e699b9b5d99167d6b27fba994d9215245cf671cf458b914e80877`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be321bf183f8a2f10257190607eee8f56ce000584dd762b27ce3518aebcc57fd`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acb94579e4a585da2995f4c9787e7e2a2bee991b0b32c72eabf497dd36fb452`  
		Last Modified: Mon, 20 Apr 2026 23:09:14 GMT  
		Size: 20.2 MB (20220932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77aed2b62f8dd25c6be38e3fab5b46266ebd4ea2997b3437c06d36df68fc52c`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3945a4a16522815c54613deb3d808ad5ead8f16aa81603d6abdaa24d3caba0da`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd670aa50e1a72277d3f64bb529f8c0c1b405016c951110ae6f38570d5a8e4f`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5231b475a9275d70c088ebeecd6c9c3fe1700aafc69aa1eb188bd3e3eb742a`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 23.5 MB (23452047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64155924f9009116e3d6e06e79a288000b5a370295cdae5f1d4c5fd0d249f974`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6488e27ba116d2e5753a6d7fc5fbcbab91a276c9048ebf533faa451482c0f70f`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799118bde74799785bee06618b18600a4d780d4cd28f0dddb41d4f4d6242ec8`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ae9d5a1287309adeabaa8d5df55128ddc09f4c801edd7f13578c07590ed96`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 11.9 MB (11948368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:4d51f373dd2a4426a1fe2dc4967a42e90a0a2c22216d9f68feffdc36302b2e1a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2126278412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8971f266b87258d9fea7ed23e99b1644fc2244c0e02ad6d1188812c524886f54`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Mon, 20 Apr 2026 23:03:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:03:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:03:10 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:03:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:19 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:03:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:03:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:03:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f4559ccd19990eeb3eb464a5c03f7c8bd4e42fc037cc850c7dc5d79bf1767`  
		Last Modified: Mon, 20 Apr 2026 23:03:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8680fed5217e07032ae763bb4814082de2b6871eea99f7bcf4be6fb17dfd79f4`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 502.1 KB (502095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542cbb5df10cc920a089a68af1d0f860484ef70c9d225a612dcf5ada2aaef390`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88dd0729e80918b82e555dffd716238e73e864506f572bbbd0a8d756ec675bf`  
		Last Modified: Mon, 20 Apr 2026 23:03:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7176f52dbf05c4190cc72cf02fbe31e6539e8dcb732de302e9ebfd1e551f86`  
		Last Modified: Mon, 20 Apr 2026 23:03:47 GMT  
		Size: 20.2 MB (20193395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30381a09bd7e612f87bec4de2b1d777841f1d46d5ba73d38f9cced6f9b8115e4`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210f368239bd3baeaccf30803eaeec62843562f847f4f963141670c760522e87`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806603dc9170bc3b136c2941f1e2a772ccfaa85ee9aef9c22b08a74e983edb3e`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ec0ed78a357c0c8f98fc6487d30563e9d8a03db4def9807966493cbf91e4ec`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 23.4 MB (23434006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3950ad53b54530338b85e919a0e803046bdb1e51c7437915640748a7a11e53`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab184fdff530ee113fb07a551306f51ac338c1ac6d707c5e5ada12e7f3a9c3`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0306647508616ca419bbaf30c1bc7c5cb266e7dacac4b59856274b4243e01`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d91cba3e753e1dc5b702a3c5be5695fcc7d24a8cd552f8c620fb10598c4cbb3`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 11.9 MB (11925928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fccccf96f59c1b8f28e7403434c83676fd2918545b80fc004f6813a8b97e16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:4d51f373dd2a4426a1fe2dc4967a42e90a0a2c22216d9f68feffdc36302b2e1a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2126278412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8971f266b87258d9fea7ed23e99b1644fc2244c0e02ad6d1188812c524886f54`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Mon, 20 Apr 2026 23:03:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:03:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:03:10 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:03:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:19 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:03:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:03:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:03:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f4559ccd19990eeb3eb464a5c03f7c8bd4e42fc037cc850c7dc5d79bf1767`  
		Last Modified: Mon, 20 Apr 2026 23:03:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8680fed5217e07032ae763bb4814082de2b6871eea99f7bcf4be6fb17dfd79f4`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 502.1 KB (502095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542cbb5df10cc920a089a68af1d0f860484ef70c9d225a612dcf5ada2aaef390`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88dd0729e80918b82e555dffd716238e73e864506f572bbbd0a8d756ec675bf`  
		Last Modified: Mon, 20 Apr 2026 23:03:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7176f52dbf05c4190cc72cf02fbe31e6539e8dcb732de302e9ebfd1e551f86`  
		Last Modified: Mon, 20 Apr 2026 23:03:47 GMT  
		Size: 20.2 MB (20193395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30381a09bd7e612f87bec4de2b1d777841f1d46d5ba73d38f9cced6f9b8115e4`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210f368239bd3baeaccf30803eaeec62843562f847f4f963141670c760522e87`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806603dc9170bc3b136c2941f1e2a772ccfaa85ee9aef9c22b08a74e983edb3e`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ec0ed78a357c0c8f98fc6487d30563e9d8a03db4def9807966493cbf91e4ec`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 23.4 MB (23434006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3950ad53b54530338b85e919a0e803046bdb1e51c7437915640748a7a11e53`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab184fdff530ee113fb07a551306f51ac338c1ac6d707c5e5ada12e7f3a9c3`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0306647508616ca419bbaf30c1bc7c5cb266e7dacac4b59856274b4243e01`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d91cba3e753e1dc5b702a3c5be5695fcc7d24a8cd552f8c620fb10598c4cbb3`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 11.9 MB (11925928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a0feb5c2dc7af77280683db28790048cd51f28ee9b61decefbe13a0518c9f308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:93470c750610123e91ad43f5b232a408d9ddd6f4bea2355e23cf1996338a8c6e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186012082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa0979c8bbd379ec0dbae2915024f4ffde2fac2bcc3ba3b496f98c9b7bd3619`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Mon, 20 Apr 2026 23:07:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:08:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:08:29 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:08:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:08:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:46 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:08:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:09:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdee3346b7a1b8ad53c9f8e5dd67903ff39beed2f224ac303b25f0dd869f8a8`  
		Last Modified: Mon, 20 Apr 2026 23:09:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa8f0463cf87863a82f8ca46c43dff6bfb2f9c87c13e93e06a6edd06c8b750`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 392.9 KB (392898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e18e138890e699b9b5d99167d6b27fba994d9215245cf671cf458b914e80877`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be321bf183f8a2f10257190607eee8f56ce000584dd762b27ce3518aebcc57fd`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acb94579e4a585da2995f4c9787e7e2a2bee991b0b32c72eabf497dd36fb452`  
		Last Modified: Mon, 20 Apr 2026 23:09:14 GMT  
		Size: 20.2 MB (20220932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77aed2b62f8dd25c6be38e3fab5b46266ebd4ea2997b3437c06d36df68fc52c`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3945a4a16522815c54613deb3d808ad5ead8f16aa81603d6abdaa24d3caba0da`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd670aa50e1a72277d3f64bb529f8c0c1b405016c951110ae6f38570d5a8e4f`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5231b475a9275d70c088ebeecd6c9c3fe1700aafc69aa1eb188bd3e3eb742a`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 23.5 MB (23452047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64155924f9009116e3d6e06e79a288000b5a370295cdae5f1d4c5fd0d249f974`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6488e27ba116d2e5753a6d7fc5fbcbab91a276c9048ebf533faa451482c0f70f`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799118bde74799785bee06618b18600a4d780d4cd28f0dddb41d4f4d6242ec8`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ae9d5a1287309adeabaa8d5df55128ddc09f4c801edd7f13578c07590ed96`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 11.9 MB (11948368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4`

```console
$ docker pull docker@sha256:c77e5d7912f9b137cc67051fdc2991d8f5ae22c55ddf532bb836dcb693a04940
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

### `docker:29.4` - linux; amd64

```console
$ docker pull docker@sha256:df0a33cee340ca6bf54b991776aa7b0adecd2f11f426e91a855205c4dede6687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140938664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b402db1b520b21284360af908099d81330e3a0abfb470068d0b691394f830f8a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:59:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:59:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:59:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:59:36 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53c3ea41339525629cfebd67afd71158e26f974aa002b648300d6b51b0a7f0`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 6.9 MB (6941788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042a8c82cc770b77ff12697783c5d4f58f4a1158c393d8d7bf48c66938dd0364`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e52c67d04087c8634de6b8e00bea30bbbfb9f44b910535df2fcf39d218a76e`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642357ac7fa1a3a23ac6950bf37044c34f3e2baf0302453327f0f0f9c07b625`  
		Last Modified: Mon, 20 Apr 2026 23:59:48 GMT  
		Size: 68.3 MB (68349083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b558d88b0e2089a0084bc1ecf86456f88572debf4e7c409c5b6a9e6a4f1c9`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c3644d4203c234122b18a9c209f1d9346bdf3ae77c865f94bb5d413b0e3ed`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:f8e5ff02cd7ab58746eba767c8cfe72659ebf0cdbc5ad53966962f5be76bb240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afcdfebb2919edf2decaff61a49a454d38f00fb49947b2a11b30fe59307eb26`

```dockerfile
```

-	Layers:
	-	`sha256:4a3c63758eb59daa26239d0a9f489fbc493b5c9520a02ee9e025dbaf9beddfcf`  
		Last Modified: Mon, 20 Apr 2026 23:59:45 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4` - linux; arm variant v6

```console
$ docker pull docker@sha256:714765536f9b13db2b7aac00ba2108c2e72491db611b2507a2dceb9cedc34edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132889403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4457d3d11f719e5294f8d032dfa5fb5584b7bb429a3c771be010f3c301a17ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:02:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:02:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:02:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:02:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:02:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:02:41 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:53 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:53 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e3ffaa23a53656a701abccec699e0622634777630e64cc504cff3d98dea60`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 8.3 MB (8297071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d350fb58b43c87a2a610f7888a7e169fbede9d23cbbf95f2f4baf73bfd058`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e71abc6298cfba6b269fcfc40efb671d56bd1a064bc669fb2569f96b3d9e98`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 18.2 MB (18156872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e844e057391513e9df6248a894061b3da111c79353463cc9293756d4682ebb`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 21.2 MB (21151868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d685033686f50b3e8f899849b292620ebe6095b84b19804734c9bf296da664`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 10.7 MB (10650797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854d1c1455463deb73d9ab0f6d7c04ba88225a33b0abf99cad5ba5be3fa9747`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ac870adbf89552657dab35d34258189f063c92bbeed903264859d2d64f304`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9337155e0b0c7eac32aafb07f862d35bdb185109213953d1e6bbf0b1f11939`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e31ea6b8650fd1cb9e50ee87e2adeb53f639a46bc5637a30509b4f2199c7a6`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 7.3 MB (7278534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05a60dd7fb89408541e99b9add9de0a0ed0fc5e1284f41dabf1dc7759413a89`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 91.7 KB (91681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb9c2c8813a470d643b478d97ee7cc9276c03c191f89e5f089c9c8af175a405`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e43bc415892250863a3c4af768f7ce347c30f4833a6a1e4a67768b501440ab`  
		Last Modified: Mon, 20 Apr 2026 23:07:06 GMT  
		Size: 63.7 MB (63682576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d001b30e4e7638598e7d353011d5b96582f31c29966d81492d68be9dabd785e`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bc8f4ddf7c3ad344ffb154ed638043188cdf4538adf0f249190938fc860463`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:47917b39931d5ff122cad720bb4846feec49fd1a70b68d9e80e0d17ce3d053fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d7b0c669a63da8adb11eee50731ea3933b923b2d3b6b3225028584b477c489`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea91ea0ce644175b943604f88c7d3ba89c5639a0373b5723b1455c6e7dd69`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4` - linux; arm variant v7

```console
$ docker pull docker@sha256:9b5665d5b82efba3f0dc4f195e3ffaefe1836577d2b82087a17f661cbdba9e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130968276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1540fdf9c9f6e2b278b27f2d4b2fffee4d93dea59718690376088e013517a488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:03:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:03:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:03:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:03:08 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:25 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67eb8b211b126a9b196c63931bfb05d72f87744ae67d6192ad13cf450e7a546`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 7.6 MB (7595775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34795d272397574b7b3e5108ed44e92aba790269dcb1bb8857915901d01f3bb`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a502b029b4b1ca6ac391718dddbb8226630ff4608fa9ad06915082bf30527a3`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 18.1 MB (18140306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b761e09f613d3b9783119e6089286c6f1ecc317627f83a2db382367f9532a`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 21.1 MB (21129738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1f0057cba8c1b61b31a0083e2b2391654b4326c8cf941fb10cdcf5c594db26`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 10.6 MB (10637140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95270af0c20972fbc14c1290b3763d03c43ce137600ca407541a323d815ea47`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff9fae5081b926ea54eabe7f33064f939afc5dda9a9eb52efb73470050f4517`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de53539477ce329ea36134755ab02f30f3d649500c60b42843af353baa1c525`  
		Last Modified: Mon, 20 Apr 2026 23:03:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efb5f9a5a71a55f54b6b99486f1bd5c1ea083613d951c96d61aaaa17077efbc`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 6.6 MB (6577240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f089c2d980079da58da3c0bec29a2b33a46373b348c2d134c18dd2431ddc248`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 88.0 KB (88020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f8cdc4960364c34cd8577f5d1b471c13ff2da3690c99299165c1073d51400`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40e7e3397d39afd124ad68cc95b2562142ff2610fce88b9aac86632e51a84f1`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 63.5 MB (63508793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ded61da57df247bd913fc7aad237f90938281d803dc83cc68b45346172aaa`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057e69e7417d0aff4a580b1aaf265dc3047522821113d8d29c120c580b8dcdea`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:31adf82453b129c500c21266951d25762d0a1d8612c4d45b214ad2ec9cde0b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcdfa8f44b536121dca093b7db18543a07667c4eccb50fc1484ddc883d5acfe`

```dockerfile
```

-	Layers:
	-	`sha256:0060530a92e8a426030ba97ebb924869a17e6a5b29719b92b59163c260a3f2d0`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ee74da04f9e09444b1d5ef2a8dbe82c89528d8de11715101b40c14a09e2cf37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130498772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a186abf796a2c5525e161a14df33c5cee12bbe6164dff8f6419f97e74b8f420`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:58:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:58:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:58:42 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b102c50bc0bd848d63594177b3551f950afb81cf23769056498c471acef763a8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 7.2 MB (7219870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffadf95cb7de624b076a0d462fa3480612216001cb1bc1977a7f7c68dd492e`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c0362756805190c2877fb2ba65ac0d7335b212c601a891a40a869a2121d2a`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6689be7b2deb380b56446eca8f0ff2610db9e7a9e33ffe8e5ce8255459333b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 61.9 MB (61854105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c32c7cfcb98ead6efe658a6dede3f1c6de4b8f676102e76dbf7519fcb80cd6`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fedc2d525bb8a19fc39fdec7b591d4dd6cbcd58ecab8ef85f4a50244792ce0b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:e5381b0fdc4555ad09b2c07b4d9a15f173eb5a42322aa01332df83c945a0bee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c928de50165b5f7d2c8e4732d512b1762d46ba6b1367c0726deefca1a9b74a8`

```dockerfile
```

-	Layers:
	-	`sha256:b37182aafc731f3098dfc2cefd626d2996f42916d78a5c3efed84580685c1ad8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-cli`

```console
$ docker pull docker@sha256:17b5c235f40be7432a7c0914c154e9278aed63bad4afe5607e4f91840696a9f8
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

### `docker:29.4-cli` - linux; amd64

```console
$ docker pull docker@sha256:ea475cbe5f579d671563e49753456303d706aa4eeaed57598aed5f976c252ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65549408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2596d6d85c20a8881389ccdca1db9b5bfdd2acbf2c9de29f2c5d68c5b7865e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8c678f6c52c4c82d7427fb6dddceeaeaf0fbc7a6450754f8d06fc88b89230084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a381a0af73b712a4aebbe9431b9ac9b119cf19ccab56ef9bc230d42208fe80`

```dockerfile
```

-	Layers:
	-	`sha256:9b00532c7328d5c1c13da3bb1a995e11d78eb22857649a7b2b898736c1b5d40a`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:1e75504955c5f006f5a647b25bebdd04958bcae39df9b5dc452f17d85f7cd892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61830622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87398cb4a53dd8a56381484fc5577e2ae102de114476ded1f78d7269bf33ada9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:02:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:02:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:02:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:02:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:02:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:02:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e3ffaa23a53656a701abccec699e0622634777630e64cc504cff3d98dea60`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 8.3 MB (8297071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d350fb58b43c87a2a610f7888a7e169fbede9d23cbbf95f2f4baf73bfd058`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e71abc6298cfba6b269fcfc40efb671d56bd1a064bc669fb2569f96b3d9e98`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 18.2 MB (18156872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e844e057391513e9df6248a894061b3da111c79353463cc9293756d4682ebb`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 21.2 MB (21151868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d685033686f50b3e8f899849b292620ebe6095b84b19804734c9bf296da664`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 10.7 MB (10650797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854d1c1455463deb73d9ab0f6d7c04ba88225a33b0abf99cad5ba5be3fa9747`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ac870adbf89552657dab35d34258189f063c92bbeed903264859d2d64f304`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9337155e0b0c7eac32aafb07f862d35bdb185109213953d1e6bbf0b1f11939`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:49bea12963a6abdd2981540b1f9f1d376ddf62a3b59bfa513300247bbc3362b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fc4edc3e7b36ff7db3bbbf4485b370c0140889b743ede632d7e904abb13280`

```dockerfile
```

-	Layers:
	-	`sha256:56e0cb7a74a706120b1715854bd1ca2075f69c6188b79bd76c37f0d35d344edb`  
		Last Modified: Mon, 20 Apr 2026 23:02:47 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b13f70e6887b08b891cda119e675ca58eae33277cc384f8c978046fa173d60a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60788235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fbaf5ba1970836d18097d7cf38e4cb04484bb6e501bee5d4106a2d77a2ff52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:03:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:03:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:03:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:03:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67eb8b211b126a9b196c63931bfb05d72f87744ae67d6192ad13cf450e7a546`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 7.6 MB (7595775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34795d272397574b7b3e5108ed44e92aba790269dcb1bb8857915901d01f3bb`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a502b029b4b1ca6ac391718dddbb8226630ff4608fa9ad06915082bf30527a3`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 18.1 MB (18140306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b761e09f613d3b9783119e6089286c6f1ecc317627f83a2db382367f9532a`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 21.1 MB (21129738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1f0057cba8c1b61b31a0083e2b2391654b4326c8cf941fb10cdcf5c594db26`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 10.6 MB (10637140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95270af0c20972fbc14c1290b3763d03c43ce137600ca407541a323d815ea47`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff9fae5081b926ea54eabe7f33064f939afc5dda9a9eb52efb73470050f4517`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de53539477ce329ea36134755ab02f30f3d649500c60b42843af353baa1c525`  
		Last Modified: Mon, 20 Apr 2026 23:03:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ae2e1d6be0d9232d64e8084bbb20b97bf932e41046e7ca77d8892c0d074a3220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2880778d01f572e158741e29a37b481691803371ae7ad079df2041fa43bd74e`

```dockerfile
```

-	Layers:
	-	`sha256:e1966d50533bdd80bf5331881d8e0ad7144144431fc76c6c5dfeb0fe82bb49ca`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:24b137d1441b41c4aa60cd5a38d069feb70e191d8c4340bcf9a7ad9b86aefb23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61317637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbbbbe92229c40c0c4fa922cff0ddafbd7d744d4652c3238ddbf132a70c1657`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3a941d5f19c61b4b5b16ad9371e7493c1548990d5cc7bddb7661c14e2572fba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e469bc2dde45b7974017a985c18538a4c3735c73f0e8c3e74cdc0e37d15f0a7a`

```dockerfile
```

-	Layers:
	-	`sha256:b845891250bf1a1824d4d301d2e389c000ebcc1e79af3839f42801d7e13f2ab5`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-dind`

```console
$ docker pull docker@sha256:c77e5d7912f9b137cc67051fdc2991d8f5ae22c55ddf532bb836dcb693a04940
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

### `docker:29.4-dind` - linux; amd64

```console
$ docker pull docker@sha256:df0a33cee340ca6bf54b991776aa7b0adecd2f11f426e91a855205c4dede6687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140938664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b402db1b520b21284360af908099d81330e3a0abfb470068d0b691394f830f8a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:59:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:59:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:59:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:59:36 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53c3ea41339525629cfebd67afd71158e26f974aa002b648300d6b51b0a7f0`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 6.9 MB (6941788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042a8c82cc770b77ff12697783c5d4f58f4a1158c393d8d7bf48c66938dd0364`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e52c67d04087c8634de6b8e00bea30bbbfb9f44b910535df2fcf39d218a76e`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642357ac7fa1a3a23ac6950bf37044c34f3e2baf0302453327f0f0f9c07b625`  
		Last Modified: Mon, 20 Apr 2026 23:59:48 GMT  
		Size: 68.3 MB (68349083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b558d88b0e2089a0084bc1ecf86456f88572debf4e7c409c5b6a9e6a4f1c9`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c3644d4203c234122b18a9c209f1d9346bdf3ae77c865f94bb5d413b0e3ed`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f8e5ff02cd7ab58746eba767c8cfe72659ebf0cdbc5ad53966962f5be76bb240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afcdfebb2919edf2decaff61a49a454d38f00fb49947b2a11b30fe59307eb26`

```dockerfile
```

-	Layers:
	-	`sha256:4a3c63758eb59daa26239d0a9f489fbc493b5c9520a02ee9e025dbaf9beddfcf`  
		Last Modified: Mon, 20 Apr 2026 23:59:45 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:714765536f9b13db2b7aac00ba2108c2e72491db611b2507a2dceb9cedc34edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132889403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4457d3d11f719e5294f8d032dfa5fb5584b7bb429a3c771be010f3c301a17ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:02:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:02:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:02:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:02:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:02:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:02:41 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:53 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:53 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e3ffaa23a53656a701abccec699e0622634777630e64cc504cff3d98dea60`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 8.3 MB (8297071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d350fb58b43c87a2a610f7888a7e169fbede9d23cbbf95f2f4baf73bfd058`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e71abc6298cfba6b269fcfc40efb671d56bd1a064bc669fb2569f96b3d9e98`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 18.2 MB (18156872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e844e057391513e9df6248a894061b3da111c79353463cc9293756d4682ebb`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 21.2 MB (21151868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d685033686f50b3e8f899849b292620ebe6095b84b19804734c9bf296da664`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 10.7 MB (10650797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854d1c1455463deb73d9ab0f6d7c04ba88225a33b0abf99cad5ba5be3fa9747`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ac870adbf89552657dab35d34258189f063c92bbeed903264859d2d64f304`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9337155e0b0c7eac32aafb07f862d35bdb185109213953d1e6bbf0b1f11939`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e31ea6b8650fd1cb9e50ee87e2adeb53f639a46bc5637a30509b4f2199c7a6`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 7.3 MB (7278534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05a60dd7fb89408541e99b9add9de0a0ed0fc5e1284f41dabf1dc7759413a89`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 91.7 KB (91681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb9c2c8813a470d643b478d97ee7cc9276c03c191f89e5f089c9c8af175a405`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e43bc415892250863a3c4af768f7ce347c30f4833a6a1e4a67768b501440ab`  
		Last Modified: Mon, 20 Apr 2026 23:07:06 GMT  
		Size: 63.7 MB (63682576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d001b30e4e7638598e7d353011d5b96582f31c29966d81492d68be9dabd785e`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bc8f4ddf7c3ad344ffb154ed638043188cdf4538adf0f249190938fc860463`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:47917b39931d5ff122cad720bb4846feec49fd1a70b68d9e80e0d17ce3d053fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d7b0c669a63da8adb11eee50731ea3933b923b2d3b6b3225028584b477c489`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea91ea0ce644175b943604f88c7d3ba89c5639a0373b5723b1455c6e7dd69`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:9b5665d5b82efba3f0dc4f195e3ffaefe1836577d2b82087a17f661cbdba9e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130968276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1540fdf9c9f6e2b278b27f2d4b2fffee4d93dea59718690376088e013517a488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:03:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:03:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:03:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:03:08 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:25 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67eb8b211b126a9b196c63931bfb05d72f87744ae67d6192ad13cf450e7a546`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 7.6 MB (7595775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34795d272397574b7b3e5108ed44e92aba790269dcb1bb8857915901d01f3bb`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a502b029b4b1ca6ac391718dddbb8226630ff4608fa9ad06915082bf30527a3`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 18.1 MB (18140306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b761e09f613d3b9783119e6089286c6f1ecc317627f83a2db382367f9532a`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 21.1 MB (21129738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1f0057cba8c1b61b31a0083e2b2391654b4326c8cf941fb10cdcf5c594db26`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 10.6 MB (10637140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95270af0c20972fbc14c1290b3763d03c43ce137600ca407541a323d815ea47`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff9fae5081b926ea54eabe7f33064f939afc5dda9a9eb52efb73470050f4517`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de53539477ce329ea36134755ab02f30f3d649500c60b42843af353baa1c525`  
		Last Modified: Mon, 20 Apr 2026 23:03:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efb5f9a5a71a55f54b6b99486f1bd5c1ea083613d951c96d61aaaa17077efbc`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 6.6 MB (6577240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f089c2d980079da58da3c0bec29a2b33a46373b348c2d134c18dd2431ddc248`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 88.0 KB (88020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f8cdc4960364c34cd8577f5d1b471c13ff2da3690c99299165c1073d51400`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40e7e3397d39afd124ad68cc95b2562142ff2610fce88b9aac86632e51a84f1`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 63.5 MB (63508793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ded61da57df247bd913fc7aad237f90938281d803dc83cc68b45346172aaa`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057e69e7417d0aff4a580b1aaf265dc3047522821113d8d29c120c580b8dcdea`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:31adf82453b129c500c21266951d25762d0a1d8612c4d45b214ad2ec9cde0b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcdfa8f44b536121dca093b7db18543a07667c4eccb50fc1484ddc883d5acfe`

```dockerfile
```

-	Layers:
	-	`sha256:0060530a92e8a426030ba97ebb924869a17e6a5b29719b92b59163c260a3f2d0`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ee74da04f9e09444b1d5ef2a8dbe82c89528d8de11715101b40c14a09e2cf37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130498772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a186abf796a2c5525e161a14df33c5cee12bbe6164dff8f6419f97e74b8f420`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:58:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:58:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:58:42 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b102c50bc0bd848d63594177b3551f950afb81cf23769056498c471acef763a8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 7.2 MB (7219870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffadf95cb7de624b076a0d462fa3480612216001cb1bc1977a7f7c68dd492e`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c0362756805190c2877fb2ba65ac0d7335b212c601a891a40a869a2121d2a`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6689be7b2deb380b56446eca8f0ff2610db9e7a9e33ffe8e5ce8255459333b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 61.9 MB (61854105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c32c7cfcb98ead6efe658a6dede3f1c6de4b8f676102e76dbf7519fcb80cd6`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fedc2d525bb8a19fc39fdec7b591d4dd6cbcd58ecab8ef85f4a50244792ce0b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e5381b0fdc4555ad09b2c07b4d9a15f173eb5a42322aa01332df83c945a0bee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c928de50165b5f7d2c8e4732d512b1762d46ba6b1367c0726deefca1a9b74a8`

```dockerfile
```

-	Layers:
	-	`sha256:b37182aafc731f3098dfc2cefd626d2996f42916d78a5c3efed84580685c1ad8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-dind-rootless`

```console
$ docker pull docker@sha256:b195ea3784d101abfe1ac68a47f95bcde74bb7ea4e4e8d277d29bc2661a6ae0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.4-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:90ee5b76cb0ac744decd66b40bf8c28137072a5c057ec0ee1929ecdbb221d36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161940861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fabb463ad72abee35979cb5448a0a39f5913b0010186d096e512ca7b033451`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:59:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:59:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:59:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:59:36 GMT
CMD []
# Tue, 21 Apr 2026 00:08:21 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 21 Apr 2026 00:08:21 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 21 Apr 2026 00:08:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 21 Apr 2026 00:08:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 21 Apr 2026 00:08:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 21 Apr 2026 00:08:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 21 Apr 2026 00:08:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53c3ea41339525629cfebd67afd71158e26f974aa002b648300d6b51b0a7f0`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 6.9 MB (6941788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042a8c82cc770b77ff12697783c5d4f58f4a1158c393d8d7bf48c66938dd0364`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e52c67d04087c8634de6b8e00bea30bbbfb9f44b910535df2fcf39d218a76e`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642357ac7fa1a3a23ac6950bf37044c34f3e2baf0302453327f0f0f9c07b625`  
		Last Modified: Mon, 20 Apr 2026 23:59:48 GMT  
		Size: 68.3 MB (68349083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b558d88b0e2089a0084bc1ecf86456f88572debf4e7c409c5b6a9e6a4f1c9`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c3644d4203c234122b18a9c209f1d9346bdf3ae77c865f94bb5d413b0e3ed`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6326f615a955ae1eaedcfd9398e20d690369774c11792fa677315a2ee4edc0eb`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 3.4 MB (3420140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab423da3008515c1f53f14584a5eec29fd4872007b06158bf377fa09ba064a75`  
		Last Modified: Tue, 21 Apr 2026 00:08:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1226b4652a0375b13cf8982005f49f46b4ea918f3afdeb0631639fbbc3314b7d`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7972f6fab882aea0a0a19ba34beda49c3a1fbc3fa74c8f1623babc91d75d88`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 17.6 MB (17580715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74b8d79d9c7fe010571a301be54bec8ec1b4d7367bd0f213d1156fd0dc66b80`  
		Last Modified: Tue, 21 Apr 2026 00:08:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1df8001a7b67a92a6737daee6dd9872da616bc3739aeaa1373577cb29a570e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670d44ba2e33335446b40d2adf46f25e8eb9622108be15df50e4e534c8d509e`

```dockerfile
```

-	Layers:
	-	`sha256:a576e6e994270734040c0f9b4683c7148fce217d815f34c6ebd4513dfc2fb099`  
		Last Modified: Tue, 21 Apr 2026 00:08:28 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a8b05ad135b3c2aaf1cc2740342e7dced62e131746edba5716795edc6ab5fe0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151777543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f34433de1df012f3564979b68c8ecbea41a0994f744ffc1a0abc1ab348b4895`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:58:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:58:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:58:42 GMT
CMD []
# Tue, 21 Apr 2026 00:08:28 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 21 Apr 2026 00:08:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 21 Apr 2026 00:08:28 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 21 Apr 2026 00:08:30 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b102c50bc0bd848d63594177b3551f950afb81cf23769056498c471acef763a8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 7.2 MB (7219870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffadf95cb7de624b076a0d462fa3480612216001cb1bc1977a7f7c68dd492e`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c0362756805190c2877fb2ba65ac0d7335b212c601a891a40a869a2121d2a`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6689be7b2deb380b56446eca8f0ff2610db9e7a9e33ffe8e5ce8255459333b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 61.9 MB (61854105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c32c7cfcb98ead6efe658a6dede3f1c6de4b8f676102e76dbf7519fcb80cd6`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fedc2d525bb8a19fc39fdec7b591d4dd6cbcd58ecab8ef85f4a50244792ce0b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef5707b49ab3f9adf26a56a9cbf6e4e78517b050e3b2fb0364f0da00f24be43`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 3.4 MB (3394528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93e0c3f1bc24f5a906884d4f60c44e459576b94f446616a5d85b9f99099e64d`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac4a74a9a53d69bcedb3a35d02f3cd37a6d429742ab1fdb508f31d983f54d86`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97af490d1d2239d0247cd840d1484d5d454ca169df2085b09c458aafd6fd0b4`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 17.9 MB (17882904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89238103243275f2a60886defdafc2cc3273f86991b81361f68cb4412a1ce84`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f2fcd0a8c8910cfe23cdc7b7f806a4a6f2a4e768fe42fff95f3b6b4bf7fa251a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77b04e174c6dfe0ab7846a82c85075337e3469d0ef0167dae8c0290864c79eb`

```dockerfile
```

-	Layers:
	-	`sha256:1e998a2dfee9b2b9098be9e582d8f43b4229d3689201c39322666ffefa251c5e`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 30.8 KB (30759 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-windowsservercore`

```console
$ docker pull docker@sha256:5106320dcd9789d033f8f0201b14e4d4e4b03061f7826fbee5f04f1beef77315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `docker:29.4-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:93470c750610123e91ad43f5b232a408d9ddd6f4bea2355e23cf1996338a8c6e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186012082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa0979c8bbd379ec0dbae2915024f4ffde2fac2bcc3ba3b496f98c9b7bd3619`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Mon, 20 Apr 2026 23:07:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:08:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:08:29 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:08:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:08:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:46 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:08:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:09:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdee3346b7a1b8ad53c9f8e5dd67903ff39beed2f224ac303b25f0dd869f8a8`  
		Last Modified: Mon, 20 Apr 2026 23:09:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa8f0463cf87863a82f8ca46c43dff6bfb2f9c87c13e93e06a6edd06c8b750`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 392.9 KB (392898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e18e138890e699b9b5d99167d6b27fba994d9215245cf671cf458b914e80877`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be321bf183f8a2f10257190607eee8f56ce000584dd762b27ce3518aebcc57fd`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acb94579e4a585da2995f4c9787e7e2a2bee991b0b32c72eabf497dd36fb452`  
		Last Modified: Mon, 20 Apr 2026 23:09:14 GMT  
		Size: 20.2 MB (20220932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77aed2b62f8dd25c6be38e3fab5b46266ebd4ea2997b3437c06d36df68fc52c`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3945a4a16522815c54613deb3d808ad5ead8f16aa81603d6abdaa24d3caba0da`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd670aa50e1a72277d3f64bb529f8c0c1b405016c951110ae6f38570d5a8e4f`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5231b475a9275d70c088ebeecd6c9c3fe1700aafc69aa1eb188bd3e3eb742a`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 23.5 MB (23452047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64155924f9009116e3d6e06e79a288000b5a370295cdae5f1d4c5fd0d249f974`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6488e27ba116d2e5753a6d7fc5fbcbab91a276c9048ebf533faa451482c0f70f`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799118bde74799785bee06618b18600a4d780d4cd28f0dddb41d4f4d6242ec8`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ae9d5a1287309adeabaa8d5df55128ddc09f4c801edd7f13578c07590ed96`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 11.9 MB (11948368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.4-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:4d51f373dd2a4426a1fe2dc4967a42e90a0a2c22216d9f68feffdc36302b2e1a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2126278412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8971f266b87258d9fea7ed23e99b1644fc2244c0e02ad6d1188812c524886f54`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Mon, 20 Apr 2026 23:03:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:03:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:03:10 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:03:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:19 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:03:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:03:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:03:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f4559ccd19990eeb3eb464a5c03f7c8bd4e42fc037cc850c7dc5d79bf1767`  
		Last Modified: Mon, 20 Apr 2026 23:03:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8680fed5217e07032ae763bb4814082de2b6871eea99f7bcf4be6fb17dfd79f4`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 502.1 KB (502095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542cbb5df10cc920a089a68af1d0f860484ef70c9d225a612dcf5ada2aaef390`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88dd0729e80918b82e555dffd716238e73e864506f572bbbd0a8d756ec675bf`  
		Last Modified: Mon, 20 Apr 2026 23:03:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7176f52dbf05c4190cc72cf02fbe31e6539e8dcb732de302e9ebfd1e551f86`  
		Last Modified: Mon, 20 Apr 2026 23:03:47 GMT  
		Size: 20.2 MB (20193395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30381a09bd7e612f87bec4de2b1d777841f1d46d5ba73d38f9cced6f9b8115e4`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210f368239bd3baeaccf30803eaeec62843562f847f4f963141670c760522e87`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806603dc9170bc3b136c2941f1e2a772ccfaa85ee9aef9c22b08a74e983edb3e`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ec0ed78a357c0c8f98fc6487d30563e9d8a03db4def9807966493cbf91e4ec`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 23.4 MB (23434006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3950ad53b54530338b85e919a0e803046bdb1e51c7437915640748a7a11e53`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab184fdff530ee113fb07a551306f51ac338c1ac6d707c5e5ada12e7f3a9c3`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0306647508616ca419bbaf30c1bc7c5cb266e7dacac4b59856274b4243e01`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d91cba3e753e1dc5b702a3c5be5695fcc7d24a8cd552f8c620fb10598c4cbb3`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 11.9 MB (11925928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fccccf96f59c1b8f28e7403434c83676fd2918545b80fc004f6813a8b97e16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `docker:29.4-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:4d51f373dd2a4426a1fe2dc4967a42e90a0a2c22216d9f68feffdc36302b2e1a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2126278412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8971f266b87258d9fea7ed23e99b1644fc2244c0e02ad6d1188812c524886f54`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Mon, 20 Apr 2026 23:03:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:03:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:03:10 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:03:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:19 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:03:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:03:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:03:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f4559ccd19990eeb3eb464a5c03f7c8bd4e42fc037cc850c7dc5d79bf1767`  
		Last Modified: Mon, 20 Apr 2026 23:03:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8680fed5217e07032ae763bb4814082de2b6871eea99f7bcf4be6fb17dfd79f4`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 502.1 KB (502095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542cbb5df10cc920a089a68af1d0f860484ef70c9d225a612dcf5ada2aaef390`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88dd0729e80918b82e555dffd716238e73e864506f572bbbd0a8d756ec675bf`  
		Last Modified: Mon, 20 Apr 2026 23:03:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7176f52dbf05c4190cc72cf02fbe31e6539e8dcb732de302e9ebfd1e551f86`  
		Last Modified: Mon, 20 Apr 2026 23:03:47 GMT  
		Size: 20.2 MB (20193395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30381a09bd7e612f87bec4de2b1d777841f1d46d5ba73d38f9cced6f9b8115e4`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210f368239bd3baeaccf30803eaeec62843562f847f4f963141670c760522e87`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806603dc9170bc3b136c2941f1e2a772ccfaa85ee9aef9c22b08a74e983edb3e`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ec0ed78a357c0c8f98fc6487d30563e9d8a03db4def9807966493cbf91e4ec`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 23.4 MB (23434006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3950ad53b54530338b85e919a0e803046bdb1e51c7437915640748a7a11e53`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab184fdff530ee113fb07a551306f51ac338c1ac6d707c5e5ada12e7f3a9c3`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0306647508616ca419bbaf30c1bc7c5cb266e7dacac4b59856274b4243e01`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d91cba3e753e1dc5b702a3c5be5695fcc7d24a8cd552f8c620fb10598c4cbb3`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 11.9 MB (11925928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a0feb5c2dc7af77280683db28790048cd51f28ee9b61decefbe13a0518c9f308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `docker:29.4-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:93470c750610123e91ad43f5b232a408d9ddd6f4bea2355e23cf1996338a8c6e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186012082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa0979c8bbd379ec0dbae2915024f4ffde2fac2bcc3ba3b496f98c9b7bd3619`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Mon, 20 Apr 2026 23:07:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:08:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:08:29 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:08:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:08:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:46 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:08:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:09:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdee3346b7a1b8ad53c9f8e5dd67903ff39beed2f224ac303b25f0dd869f8a8`  
		Last Modified: Mon, 20 Apr 2026 23:09:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa8f0463cf87863a82f8ca46c43dff6bfb2f9c87c13e93e06a6edd06c8b750`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 392.9 KB (392898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e18e138890e699b9b5d99167d6b27fba994d9215245cf671cf458b914e80877`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be321bf183f8a2f10257190607eee8f56ce000584dd762b27ce3518aebcc57fd`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acb94579e4a585da2995f4c9787e7e2a2bee991b0b32c72eabf497dd36fb452`  
		Last Modified: Mon, 20 Apr 2026 23:09:14 GMT  
		Size: 20.2 MB (20220932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77aed2b62f8dd25c6be38e3fab5b46266ebd4ea2997b3437c06d36df68fc52c`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3945a4a16522815c54613deb3d808ad5ead8f16aa81603d6abdaa24d3caba0da`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd670aa50e1a72277d3f64bb529f8c0c1b405016c951110ae6f38570d5a8e4f`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5231b475a9275d70c088ebeecd6c9c3fe1700aafc69aa1eb188bd3e3eb742a`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 23.5 MB (23452047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64155924f9009116e3d6e06e79a288000b5a370295cdae5f1d4c5fd0d249f974`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6488e27ba116d2e5753a6d7fc5fbcbab91a276c9048ebf533faa451482c0f70f`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799118bde74799785bee06618b18600a4d780d4cd28f0dddb41d4f4d6242ec8`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ae9d5a1287309adeabaa8d5df55128ddc09f4c801edd7f13578c07590ed96`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 11.9 MB (11948368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4.3`

**does not exist** (yet?)

## `docker:29.4.3-alpine3.23`

**does not exist** (yet?)

## `docker:29.4.3-cli`

**does not exist** (yet?)

## `docker:29.4.3-cli-alpine3.23`

**does not exist** (yet?)

## `docker:29.4.3-dind`

**does not exist** (yet?)

## `docker:29.4.3-dind-alpine3.23`

**does not exist** (yet?)

## `docker:29.4.3-dind-rootless`

**does not exist** (yet?)

## `docker:29.4.3-windowsservercore`

**does not exist** (yet?)

## `docker:29.4.3-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `docker:29.4.3-windowsservercore-ltsc2025`

**does not exist** (yet?)

## `docker:cli`

```console
$ docker pull docker@sha256:17b5c235f40be7432a7c0914c154e9278aed63bad4afe5607e4f91840696a9f8
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
$ docker pull docker@sha256:ea475cbe5f579d671563e49753456303d706aa4eeaed57598aed5f976c252ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65549408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2596d6d85c20a8881389ccdca1db9b5bfdd2acbf2c9de29f2c5d68c5b7865e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:8c678f6c52c4c82d7427fb6dddceeaeaf0fbc7a6450754f8d06fc88b89230084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a381a0af73b712a4aebbe9431b9ac9b119cf19ccab56ef9bc230d42208fe80`

```dockerfile
```

-	Layers:
	-	`sha256:9b00532c7328d5c1c13da3bb1a995e11d78eb22857649a7b2b898736c1b5d40a`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:1e75504955c5f006f5a647b25bebdd04958bcae39df9b5dc452f17d85f7cd892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61830622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87398cb4a53dd8a56381484fc5577e2ae102de114476ded1f78d7269bf33ada9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:02:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:02:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:02:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:02:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:02:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:02:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e3ffaa23a53656a701abccec699e0622634777630e64cc504cff3d98dea60`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 8.3 MB (8297071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d350fb58b43c87a2a610f7888a7e169fbede9d23cbbf95f2f4baf73bfd058`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e71abc6298cfba6b269fcfc40efb671d56bd1a064bc669fb2569f96b3d9e98`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 18.2 MB (18156872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e844e057391513e9df6248a894061b3da111c79353463cc9293756d4682ebb`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 21.2 MB (21151868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d685033686f50b3e8f899849b292620ebe6095b84b19804734c9bf296da664`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 10.7 MB (10650797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854d1c1455463deb73d9ab0f6d7c04ba88225a33b0abf99cad5ba5be3fa9747`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ac870adbf89552657dab35d34258189f063c92bbeed903264859d2d64f304`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9337155e0b0c7eac32aafb07f862d35bdb185109213953d1e6bbf0b1f11939`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:49bea12963a6abdd2981540b1f9f1d376ddf62a3b59bfa513300247bbc3362b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fc4edc3e7b36ff7db3bbbf4485b370c0140889b743ede632d7e904abb13280`

```dockerfile
```

-	Layers:
	-	`sha256:56e0cb7a74a706120b1715854bd1ca2075f69c6188b79bd76c37f0d35d344edb`  
		Last Modified: Mon, 20 Apr 2026 23:02:47 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b13f70e6887b08b891cda119e675ca58eae33277cc384f8c978046fa173d60a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60788235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fbaf5ba1970836d18097d7cf38e4cb04484bb6e501bee5d4106a2d77a2ff52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:03:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:03:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:03:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:03:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67eb8b211b126a9b196c63931bfb05d72f87744ae67d6192ad13cf450e7a546`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 7.6 MB (7595775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34795d272397574b7b3e5108ed44e92aba790269dcb1bb8857915901d01f3bb`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a502b029b4b1ca6ac391718dddbb8226630ff4608fa9ad06915082bf30527a3`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 18.1 MB (18140306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b761e09f613d3b9783119e6089286c6f1ecc317627f83a2db382367f9532a`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 21.1 MB (21129738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1f0057cba8c1b61b31a0083e2b2391654b4326c8cf941fb10cdcf5c594db26`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 10.6 MB (10637140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95270af0c20972fbc14c1290b3763d03c43ce137600ca407541a323d815ea47`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff9fae5081b926ea54eabe7f33064f939afc5dda9a9eb52efb73470050f4517`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de53539477ce329ea36134755ab02f30f3d649500c60b42843af353baa1c525`  
		Last Modified: Mon, 20 Apr 2026 23:03:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:ae2e1d6be0d9232d64e8084bbb20b97bf932e41046e7ca77d8892c0d074a3220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2880778d01f572e158741e29a37b481691803371ae7ad079df2041fa43bd74e`

```dockerfile
```

-	Layers:
	-	`sha256:e1966d50533bdd80bf5331881d8e0ad7144144431fc76c6c5dfeb0fe82bb49ca`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:24b137d1441b41c4aa60cd5a38d069feb70e191d8c4340bcf9a7ad9b86aefb23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61317637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbbbbe92229c40c0c4fa922cff0ddafbd7d744d4652c3238ddbf132a70c1657`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:3a941d5f19c61b4b5b16ad9371e7493c1548990d5cc7bddb7661c14e2572fba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e469bc2dde45b7974017a985c18538a4c3735c73f0e8c3e74cdc0e37d15f0a7a`

```dockerfile
```

-	Layers:
	-	`sha256:b845891250bf1a1824d4d301d2e389c000ebcc1e79af3839f42801d7e13f2ab5`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 38.3 KB (38262 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:c77e5d7912f9b137cc67051fdc2991d8f5ae22c55ddf532bb836dcb693a04940
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
$ docker pull docker@sha256:df0a33cee340ca6bf54b991776aa7b0adecd2f11f426e91a855205c4dede6687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140938664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b402db1b520b21284360af908099d81330e3a0abfb470068d0b691394f830f8a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:59:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:59:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:59:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:59:36 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53c3ea41339525629cfebd67afd71158e26f974aa002b648300d6b51b0a7f0`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 6.9 MB (6941788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042a8c82cc770b77ff12697783c5d4f58f4a1158c393d8d7bf48c66938dd0364`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e52c67d04087c8634de6b8e00bea30bbbfb9f44b910535df2fcf39d218a76e`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642357ac7fa1a3a23ac6950bf37044c34f3e2baf0302453327f0f0f9c07b625`  
		Last Modified: Mon, 20 Apr 2026 23:59:48 GMT  
		Size: 68.3 MB (68349083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b558d88b0e2089a0084bc1ecf86456f88572debf4e7c409c5b6a9e6a4f1c9`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c3644d4203c234122b18a9c209f1d9346bdf3ae77c865f94bb5d413b0e3ed`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:f8e5ff02cd7ab58746eba767c8cfe72659ebf0cdbc5ad53966962f5be76bb240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afcdfebb2919edf2decaff61a49a454d38f00fb49947b2a11b30fe59307eb26`

```dockerfile
```

-	Layers:
	-	`sha256:4a3c63758eb59daa26239d0a9f489fbc493b5c9520a02ee9e025dbaf9beddfcf`  
		Last Modified: Mon, 20 Apr 2026 23:59:45 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:714765536f9b13db2b7aac00ba2108c2e72491db611b2507a2dceb9cedc34edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132889403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4457d3d11f719e5294f8d032dfa5fb5584b7bb429a3c771be010f3c301a17ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:02:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:02:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:02:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:02:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:02:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:02:41 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:53 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:53 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e3ffaa23a53656a701abccec699e0622634777630e64cc504cff3d98dea60`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 8.3 MB (8297071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d350fb58b43c87a2a610f7888a7e169fbede9d23cbbf95f2f4baf73bfd058`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e71abc6298cfba6b269fcfc40efb671d56bd1a064bc669fb2569f96b3d9e98`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 18.2 MB (18156872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e844e057391513e9df6248a894061b3da111c79353463cc9293756d4682ebb`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 21.2 MB (21151868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d685033686f50b3e8f899849b292620ebe6095b84b19804734c9bf296da664`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 10.7 MB (10650797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854d1c1455463deb73d9ab0f6d7c04ba88225a33b0abf99cad5ba5be3fa9747`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ac870adbf89552657dab35d34258189f063c92bbeed903264859d2d64f304`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9337155e0b0c7eac32aafb07f862d35bdb185109213953d1e6bbf0b1f11939`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e31ea6b8650fd1cb9e50ee87e2adeb53f639a46bc5637a30509b4f2199c7a6`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 7.3 MB (7278534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05a60dd7fb89408541e99b9add9de0a0ed0fc5e1284f41dabf1dc7759413a89`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 91.7 KB (91681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb9c2c8813a470d643b478d97ee7cc9276c03c191f89e5f089c9c8af175a405`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e43bc415892250863a3c4af768f7ce347c30f4833a6a1e4a67768b501440ab`  
		Last Modified: Mon, 20 Apr 2026 23:07:06 GMT  
		Size: 63.7 MB (63682576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d001b30e4e7638598e7d353011d5b96582f31c29966d81492d68be9dabd785e`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bc8f4ddf7c3ad344ffb154ed638043188cdf4538adf0f249190938fc860463`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:47917b39931d5ff122cad720bb4846feec49fd1a70b68d9e80e0d17ce3d053fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d7b0c669a63da8adb11eee50731ea3933b923b2d3b6b3225028584b477c489`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea91ea0ce644175b943604f88c7d3ba89c5639a0373b5723b1455c6e7dd69`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:9b5665d5b82efba3f0dc4f195e3ffaefe1836577d2b82087a17f661cbdba9e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130968276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1540fdf9c9f6e2b278b27f2d4b2fffee4d93dea59718690376088e013517a488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:03:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:03:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:03:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:03:08 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:25 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67eb8b211b126a9b196c63931bfb05d72f87744ae67d6192ad13cf450e7a546`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 7.6 MB (7595775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34795d272397574b7b3e5108ed44e92aba790269dcb1bb8857915901d01f3bb`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a502b029b4b1ca6ac391718dddbb8226630ff4608fa9ad06915082bf30527a3`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 18.1 MB (18140306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b761e09f613d3b9783119e6089286c6f1ecc317627f83a2db382367f9532a`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 21.1 MB (21129738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1f0057cba8c1b61b31a0083e2b2391654b4326c8cf941fb10cdcf5c594db26`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 10.6 MB (10637140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95270af0c20972fbc14c1290b3763d03c43ce137600ca407541a323d815ea47`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff9fae5081b926ea54eabe7f33064f939afc5dda9a9eb52efb73470050f4517`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de53539477ce329ea36134755ab02f30f3d649500c60b42843af353baa1c525`  
		Last Modified: Mon, 20 Apr 2026 23:03:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efb5f9a5a71a55f54b6b99486f1bd5c1ea083613d951c96d61aaaa17077efbc`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 6.6 MB (6577240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f089c2d980079da58da3c0bec29a2b33a46373b348c2d134c18dd2431ddc248`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 88.0 KB (88020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f8cdc4960364c34cd8577f5d1b471c13ff2da3690c99299165c1073d51400`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40e7e3397d39afd124ad68cc95b2562142ff2610fce88b9aac86632e51a84f1`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 63.5 MB (63508793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ded61da57df247bd913fc7aad237f90938281d803dc83cc68b45346172aaa`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057e69e7417d0aff4a580b1aaf265dc3047522821113d8d29c120c580b8dcdea`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:31adf82453b129c500c21266951d25762d0a1d8612c4d45b214ad2ec9cde0b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcdfa8f44b536121dca093b7db18543a07667c4eccb50fc1484ddc883d5acfe`

```dockerfile
```

-	Layers:
	-	`sha256:0060530a92e8a426030ba97ebb924869a17e6a5b29719b92b59163c260a3f2d0`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ee74da04f9e09444b1d5ef2a8dbe82c89528d8de11715101b40c14a09e2cf37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130498772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a186abf796a2c5525e161a14df33c5cee12bbe6164dff8f6419f97e74b8f420`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:58:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:58:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:58:42 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b102c50bc0bd848d63594177b3551f950afb81cf23769056498c471acef763a8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 7.2 MB (7219870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffadf95cb7de624b076a0d462fa3480612216001cb1bc1977a7f7c68dd492e`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c0362756805190c2877fb2ba65ac0d7335b212c601a891a40a869a2121d2a`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6689be7b2deb380b56446eca8f0ff2610db9e7a9e33ffe8e5ce8255459333b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 61.9 MB (61854105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c32c7cfcb98ead6efe658a6dede3f1c6de4b8f676102e76dbf7519fcb80cd6`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fedc2d525bb8a19fc39fdec7b591d4dd6cbcd58ecab8ef85f4a50244792ce0b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e5381b0fdc4555ad09b2c07b4d9a15f173eb5a42322aa01332df83c945a0bee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c928de50165b5f7d2c8e4732d512b1762d46ba6b1367c0726deefca1a9b74a8`

```dockerfile
```

-	Layers:
	-	`sha256:b37182aafc731f3098dfc2cefd626d2996f42916d78a5c3efed84580685c1ad8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:b195ea3784d101abfe1ac68a47f95bcde74bb7ea4e4e8d277d29bc2661a6ae0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:90ee5b76cb0ac744decd66b40bf8c28137072a5c057ec0ee1929ecdbb221d36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161940861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fabb463ad72abee35979cb5448a0a39f5913b0010186d096e512ca7b033451`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:59:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:59:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:59:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:59:36 GMT
CMD []
# Tue, 21 Apr 2026 00:08:21 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 21 Apr 2026 00:08:21 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 21 Apr 2026 00:08:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 21 Apr 2026 00:08:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 21 Apr 2026 00:08:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 21 Apr 2026 00:08:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 21 Apr 2026 00:08:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53c3ea41339525629cfebd67afd71158e26f974aa002b648300d6b51b0a7f0`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 6.9 MB (6941788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042a8c82cc770b77ff12697783c5d4f58f4a1158c393d8d7bf48c66938dd0364`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e52c67d04087c8634de6b8e00bea30bbbfb9f44b910535df2fcf39d218a76e`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642357ac7fa1a3a23ac6950bf37044c34f3e2baf0302453327f0f0f9c07b625`  
		Last Modified: Mon, 20 Apr 2026 23:59:48 GMT  
		Size: 68.3 MB (68349083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b558d88b0e2089a0084bc1ecf86456f88572debf4e7c409c5b6a9e6a4f1c9`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c3644d4203c234122b18a9c209f1d9346bdf3ae77c865f94bb5d413b0e3ed`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6326f615a955ae1eaedcfd9398e20d690369774c11792fa677315a2ee4edc0eb`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 3.4 MB (3420140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab423da3008515c1f53f14584a5eec29fd4872007b06158bf377fa09ba064a75`  
		Last Modified: Tue, 21 Apr 2026 00:08:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1226b4652a0375b13cf8982005f49f46b4ea918f3afdeb0631639fbbc3314b7d`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7972f6fab882aea0a0a19ba34beda49c3a1fbc3fa74c8f1623babc91d75d88`  
		Last Modified: Tue, 21 Apr 2026 00:08:29 GMT  
		Size: 17.6 MB (17580715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74b8d79d9c7fe010571a301be54bec8ec1b4d7367bd0f213d1156fd0dc66b80`  
		Last Modified: Tue, 21 Apr 2026 00:08:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1df8001a7b67a92a6737daee6dd9872da616bc3739aeaa1373577cb29a570e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670d44ba2e33335446b40d2adf46f25e8eb9622108be15df50e4e534c8d509e`

```dockerfile
```

-	Layers:
	-	`sha256:a576e6e994270734040c0f9b4683c7148fce217d815f34c6ebd4513dfc2fb099`  
		Last Modified: Tue, 21 Apr 2026 00:08:28 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a8b05ad135b3c2aaf1cc2740342e7dced62e131746edba5716795edc6ab5fe0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151777543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f34433de1df012f3564979b68c8ecbea41a0994f744ffc1a0abc1ab348b4895`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:58:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:58:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:58:42 GMT
CMD []
# Tue, 21 Apr 2026 00:08:28 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 21 Apr 2026 00:08:28 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 21 Apr 2026 00:08:28 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 21 Apr 2026 00:08:30 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 21 Apr 2026 00:08:30 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b102c50bc0bd848d63594177b3551f950afb81cf23769056498c471acef763a8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 7.2 MB (7219870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffadf95cb7de624b076a0d462fa3480612216001cb1bc1977a7f7c68dd492e`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c0362756805190c2877fb2ba65ac0d7335b212c601a891a40a869a2121d2a`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6689be7b2deb380b56446eca8f0ff2610db9e7a9e33ffe8e5ce8255459333b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 61.9 MB (61854105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c32c7cfcb98ead6efe658a6dede3f1c6de4b8f676102e76dbf7519fcb80cd6`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fedc2d525bb8a19fc39fdec7b591d4dd6cbcd58ecab8ef85f4a50244792ce0b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef5707b49ab3f9adf26a56a9cbf6e4e78517b050e3b2fb0364f0da00f24be43`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 3.4 MB (3394528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93e0c3f1bc24f5a906884d4f60c44e459576b94f446616a5d85b9f99099e64d`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac4a74a9a53d69bcedb3a35d02f3cd37a6d429742ab1fdb508f31d983f54d86`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97af490d1d2239d0247cd840d1484d5d454ca169df2085b09c458aafd6fd0b4`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 17.9 MB (17882904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89238103243275f2a60886defdafc2cc3273f86991b81361f68cb4412a1ce84`  
		Last Modified: Tue, 21 Apr 2026 00:08:36 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f2fcd0a8c8910cfe23cdc7b7f806a4a6f2a4e768fe42fff95f3b6b4bf7fa251a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77b04e174c6dfe0ab7846a82c85075337e3469d0ef0167dae8c0290864c79eb`

```dockerfile
```

-	Layers:
	-	`sha256:1e998a2dfee9b2b9098be9e582d8f43b4229d3689201c39322666ffefa251c5e`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 30.8 KB (30759 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:c77e5d7912f9b137cc67051fdc2991d8f5ae22c55ddf532bb836dcb693a04940
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
$ docker pull docker@sha256:df0a33cee340ca6bf54b991776aa7b0adecd2f11f426e91a855205c4dede6687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140938664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b402db1b520b21284360af908099d81330e3a0abfb470068d0b691394f830f8a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:18:06 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:18:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:18:09 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:18:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:18:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:10 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:59:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:59:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:59:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:59:36 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:59:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:59:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:59:36 GMT
CMD []
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e4e9c4f17127ca5ebf5bdc2c6d697c94f074019bf71396dd5c22479d03241b`  
		Last Modified: Mon, 20 Apr 2026 23:18:17 GMT  
		Size: 8.4 MB (8390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5a18659b1fc946acaaa7d3ff50a916e1a50f1b2d1631aa985e49d28e7fa18`  
		Last Modified: Mon, 20 Apr 2026 23:18:16 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aad62b317614753c87ddb204b72f7d9a5274168de009b617645952348dbab6`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 19.5 MB (19509767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202d21d268cd90606683707c2f836157949013005af213bd9701929aac3e0f1`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 22.5 MB (22539230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9e6578d781aeeaec3c48750a80267dd5c672936132056160840e0ab863867`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 11.2 MB (11243751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704fb81a37c3aaf303920eb4916e6cffbcfc0fd3e92c576d2c919c80fe76cf34`  
		Last Modified: Mon, 20 Apr 2026 23:18:18 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d5a3c6758df8b5ce7a9e9770470e6def02793603fc58fad8b70537120860b`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d983ea1647a22299dae6ff9c66735c0c24d8ddbc170d29722f63d3d702354ed`  
		Last Modified: Mon, 20 Apr 2026 23:18:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53c3ea41339525629cfebd67afd71158e26f974aa002b648300d6b51b0a7f0`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 6.9 MB (6941788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042a8c82cc770b77ff12697783c5d4f58f4a1158c393d8d7bf48c66938dd0364`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 92.4 KB (92386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e52c67d04087c8634de6b8e00bea30bbbfb9f44b910535df2fcf39d218a76e`  
		Last Modified: Mon, 20 Apr 2026 23:59:46 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642357ac7fa1a3a23ac6950bf37044c34f3e2baf0302453327f0f0f9c07b625`  
		Last Modified: Mon, 20 Apr 2026 23:59:48 GMT  
		Size: 68.3 MB (68349083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b558d88b0e2089a0084bc1ecf86456f88572debf4e7c409c5b6a9e6a4f1c9`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c3644d4203c234122b18a9c209f1d9346bdf3ae77c865f94bb5d413b0e3ed`  
		Last Modified: Mon, 20 Apr 2026 23:59:47 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:f8e5ff02cd7ab58746eba767c8cfe72659ebf0cdbc5ad53966962f5be76bb240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afcdfebb2919edf2decaff61a49a454d38f00fb49947b2a11b30fe59307eb26`

```dockerfile
```

-	Layers:
	-	`sha256:4a3c63758eb59daa26239d0a9f489fbc493b5c9520a02ee9e025dbaf9beddfcf`  
		Last Modified: Mon, 20 Apr 2026 23:59:45 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:714765536f9b13db2b7aac00ba2108c2e72491db611b2507a2dceb9cedc34edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132889403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4457d3d11f719e5294f8d032dfa5fb5584b7bb429a3c771be010f3c301a17ae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:02:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:02:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:02:37 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:02:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:02:39 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:02:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:02:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:02:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:02:41 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:49 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:53 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:53 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:53 GMT
CMD []
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e3ffaa23a53656a701abccec699e0622634777630e64cc504cff3d98dea60`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 8.3 MB (8297071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012d350fb58b43c87a2a610f7888a7e169fbede9d23cbbf95f2f4baf73bfd058`  
		Last Modified: Mon, 20 Apr 2026 23:02:48 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e71abc6298cfba6b269fcfc40efb671d56bd1a064bc669fb2569f96b3d9e98`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 18.2 MB (18156872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e844e057391513e9df6248a894061b3da111c79353463cc9293756d4682ebb`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 21.2 MB (21151868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d685033686f50b3e8f899849b292620ebe6095b84b19804734c9bf296da664`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 10.7 MB (10650797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854d1c1455463deb73d9ab0f6d7c04ba88225a33b0abf99cad5ba5be3fa9747`  
		Last Modified: Mon, 20 Apr 2026 23:02:49 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ac870adbf89552657dab35d34258189f063c92bbeed903264859d2d64f304`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9337155e0b0c7eac32aafb07f862d35bdb185109213953d1e6bbf0b1f11939`  
		Last Modified: Mon, 20 Apr 2026 23:02:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e31ea6b8650fd1cb9e50ee87e2adeb53f639a46bc5637a30509b4f2199c7a6`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 7.3 MB (7278534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05a60dd7fb89408541e99b9add9de0a0ed0fc5e1284f41dabf1dc7759413a89`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 91.7 KB (91681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb9c2c8813a470d643b478d97ee7cc9276c03c191f89e5f089c9c8af175a405`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e43bc415892250863a3c4af768f7ce347c30f4833a6a1e4a67768b501440ab`  
		Last Modified: Mon, 20 Apr 2026 23:07:06 GMT  
		Size: 63.7 MB (63682576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d001b30e4e7638598e7d353011d5b96582f31c29966d81492d68be9dabd785e`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bc8f4ddf7c3ad344ffb154ed638043188cdf4538adf0f249190938fc860463`  
		Last Modified: Mon, 20 Apr 2026 23:07:05 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:47917b39931d5ff122cad720bb4846feec49fd1a70b68d9e80e0d17ce3d053fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d7b0c669a63da8adb11eee50731ea3933b923b2d3b6b3225028584b477c489`

```dockerfile
```

-	Layers:
	-	`sha256:b8aea91ea0ce644175b943604f88c7d3ba89c5639a0373b5723b1455c6e7dd69`  
		Last Modified: Mon, 20 Apr 2026 23:07:04 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:9b5665d5b82efba3f0dc4f195e3ffaefe1836577d2b82087a17f661cbdba9e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130968276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1540fdf9c9f6e2b278b27f2d4b2fffee4d93dea59718690376088e013517a488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:03:00 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:03:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:03:03 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:03:06 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:03:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:03:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:03:08 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:06:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:06:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:06:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:06:25 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:06:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:06:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:25 GMT
CMD []
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67eb8b211b126a9b196c63931bfb05d72f87744ae67d6192ad13cf450e7a546`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 7.6 MB (7595775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34795d272397574b7b3e5108ed44e92aba790269dcb1bb8857915901d01f3bb`  
		Last Modified: Mon, 20 Apr 2026 23:03:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a502b029b4b1ca6ac391718dddbb8226630ff4608fa9ad06915082bf30527a3`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 18.1 MB (18140306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b761e09f613d3b9783119e6089286c6f1ecc317627f83a2db382367f9532a`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 21.1 MB (21129738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1f0057cba8c1b61b31a0083e2b2391654b4326c8cf941fb10cdcf5c594db26`  
		Last Modified: Mon, 20 Apr 2026 23:03:15 GMT  
		Size: 10.6 MB (10637140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95270af0c20972fbc14c1290b3763d03c43ce137600ca407541a323d815ea47`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff9fae5081b926ea54eabe7f33064f939afc5dda9a9eb52efb73470050f4517`  
		Last Modified: Mon, 20 Apr 2026 23:03:16 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de53539477ce329ea36134755ab02f30f3d649500c60b42843af353baa1c525`  
		Last Modified: Mon, 20 Apr 2026 23:03:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efb5f9a5a71a55f54b6b99486f1bd5c1ea083613d951c96d61aaaa17077efbc`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 6.6 MB (6577240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f089c2d980079da58da3c0bec29a2b33a46373b348c2d134c18dd2431ddc248`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 88.0 KB (88020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f8cdc4960364c34cd8577f5d1b471c13ff2da3690c99299165c1073d51400`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40e7e3397d39afd124ad68cc95b2562142ff2610fce88b9aac86632e51a84f1`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 63.5 MB (63508793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0ded61da57df247bd913fc7aad237f90938281d803dc83cc68b45346172aaa`  
		Last Modified: Mon, 20 Apr 2026 23:06:36 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057e69e7417d0aff4a580b1aaf265dc3047522821113d8d29c120c580b8dcdea`  
		Last Modified: Mon, 20 Apr 2026 23:06:37 GMT  
		Size: 3.3 KB (3295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:31adf82453b129c500c21266951d25762d0a1d8612c4d45b214ad2ec9cde0b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcdfa8f44b536121dca093b7db18543a07667c4eccb50fc1484ddc883d5acfe`

```dockerfile
```

-	Layers:
	-	`sha256:0060530a92e8a426030ba97ebb924869a17e6a5b29719b92b59163c260a3f2d0`  
		Last Modified: Mon, 20 Apr 2026 23:06:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ee74da04f9e09444b1d5ef2a8dbe82c89528d8de11715101b40c14a09e2cf37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130498772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a186abf796a2c5525e161a14df33c5cee12bbe6164dff8f6419f97e74b8f420`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:13:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:13:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:13:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 20 Apr 2026 23:13:49 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:13:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 20 Apr 2026 23:13:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:13:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-x86_64'; 			sha256='a0298760c9772d2c06888fc8703a487c94c3c3b0134adeef830742a2fc7647b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv6'; 			sha256='514fc01481017bf4ae55a3b1fe7d598ca49a930e346803648bd88dba9d4ae3da'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-armv7'; 			sha256='4c1ce6ad43c184934a1f76cd55d7231192492c487acbd13e96258ed10fd9e468'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-aarch64'; 			sha256='e8105a3e687ea7e0b0f81abe4bf9269c8a2801fb72c2b498b5ff2472bc54145f'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-ppc64le'; 			sha256='ceaa1a9f24ef471e6f9fc34b30d11dcb6d8021a9a283c5e7261521ef12951432'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-riscv64'; 			sha256='f4a01e52ab7b14bc88e0657f6c477274f151c7907cfe6a5362709f7bd4814c44'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-linux-s390x'; 			sha256='552d11a594aa3d81b4b69a2abd2a5c2e699378038a8efaa8200c0b556be3451f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 20 Apr 2026 23:13:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 20 Apr 2026 23:13:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:13:51 GMT
CMD ["sh"]
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 20 Apr 2026 23:58:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 20 Apr 2026 23:58:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:58:42 GMT
VOLUME [/var/lib/docker]
# Mon, 20 Apr 2026 23:58:42 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 20 Apr 2026 23:58:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 20 Apr 2026 23:58:42 GMT
CMD []
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e76997616dee16ecda265e1cec224428f4f9af00cbc0d8b0c1bfe291218ebe`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 8.5 MB (8450102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90cf62ec7783763d2b792410f3bd9905e0f97f591438f0d0b47d50cba91461a`  
		Last Modified: Mon, 20 Apr 2026 23:13:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b130c2bf4020b98fbfe9b72851a9a69b45461a76cafd89592f931fe68b3ba8`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 18.0 MB (17969135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf85db8a55da2125e47f1fa9beca5db3068748062b2005d6c2dac0707c895bc`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 20.5 MB (20453111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdb2d146c58478f629218f7cec0b57133719dac8888f9f9d1a806e784b6aa44`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 10.2 MB (10243270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fad7f32e3fa28a617acfa9e40432cc1feb004951cb69a731b8c232e0a4a0c9`  
		Last Modified: Mon, 20 Apr 2026 23:13:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3539a42c5573abd62f988c1d2f79eb496b6538c80c809eeeabf4e6dc7ceb34`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349f2f8a8b1bc5894eb45df1712f8f6ea1555ae0bb34b32bd7c153000f55ada2`  
		Last Modified: Mon, 20 Apr 2026 23:13:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b102c50bc0bd848d63594177b3551f950afb81cf23769056498c471acef763a8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 7.2 MB (7219870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffadf95cb7de624b076a0d462fa3480612216001cb1bc1977a7f7c68dd492e`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 101.2 KB (101158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c0362756805190c2877fb2ba65ac0d7335b212c601a891a40a869a2121d2a`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6689be7b2deb380b56446eca8f0ff2610db9e7a9e33ffe8e5ce8255459333b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 61.9 MB (61854105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c32c7cfcb98ead6efe658a6dede3f1c6de4b8f676102e76dbf7519fcb80cd6`  
		Last Modified: Mon, 20 Apr 2026 23:58:53 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fedc2d525bb8a19fc39fdec7b591d4dd6cbcd58ecab8ef85f4a50244792ce0b`  
		Last Modified: Mon, 20 Apr 2026 23:58:54 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:e5381b0fdc4555ad09b2c07b4d9a15f173eb5a42322aa01332df83c945a0bee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c928de50165b5f7d2c8e4732d512b1762d46ba6b1367c0726deefca1a9b74a8`

```dockerfile
```

-	Layers:
	-	`sha256:b37182aafc731f3098dfc2cefd626d2996f42916d78a5c3efed84580685c1ad8`  
		Last Modified: Mon, 20 Apr 2026 23:58:52 GMT  
		Size: 34.8 KB (34783 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:5106320dcd9789d033f8f0201b14e4d4e4b03061f7826fbee5f04f1beef77315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:93470c750610123e91ad43f5b232a408d9ddd6f4bea2355e23cf1996338a8c6e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186012082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa0979c8bbd379ec0dbae2915024f4ffde2fac2bcc3ba3b496f98c9b7bd3619`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Mon, 20 Apr 2026 23:07:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:08:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:08:29 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:08:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:08:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:46 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:08:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:09:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdee3346b7a1b8ad53c9f8e5dd67903ff39beed2f224ac303b25f0dd869f8a8`  
		Last Modified: Mon, 20 Apr 2026 23:09:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa8f0463cf87863a82f8ca46c43dff6bfb2f9c87c13e93e06a6edd06c8b750`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 392.9 KB (392898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e18e138890e699b9b5d99167d6b27fba994d9215245cf671cf458b914e80877`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be321bf183f8a2f10257190607eee8f56ce000584dd762b27ce3518aebcc57fd`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acb94579e4a585da2995f4c9787e7e2a2bee991b0b32c72eabf497dd36fb452`  
		Last Modified: Mon, 20 Apr 2026 23:09:14 GMT  
		Size: 20.2 MB (20220932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77aed2b62f8dd25c6be38e3fab5b46266ebd4ea2997b3437c06d36df68fc52c`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3945a4a16522815c54613deb3d808ad5ead8f16aa81603d6abdaa24d3caba0da`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd670aa50e1a72277d3f64bb529f8c0c1b405016c951110ae6f38570d5a8e4f`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5231b475a9275d70c088ebeecd6c9c3fe1700aafc69aa1eb188bd3e3eb742a`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 23.5 MB (23452047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64155924f9009116e3d6e06e79a288000b5a370295cdae5f1d4c5fd0d249f974`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6488e27ba116d2e5753a6d7fc5fbcbab91a276c9048ebf533faa451482c0f70f`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799118bde74799785bee06618b18600a4d780d4cd28f0dddb41d4f4d6242ec8`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ae9d5a1287309adeabaa8d5df55128ddc09f4c801edd7f13578c07590ed96`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 11.9 MB (11948368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:4d51f373dd2a4426a1fe2dc4967a42e90a0a2c22216d9f68feffdc36302b2e1a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2126278412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8971f266b87258d9fea7ed23e99b1644fc2244c0e02ad6d1188812c524886f54`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Mon, 20 Apr 2026 23:03:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:03:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:03:10 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:03:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:19 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:03:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:03:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:03:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f4559ccd19990eeb3eb464a5c03f7c8bd4e42fc037cc850c7dc5d79bf1767`  
		Last Modified: Mon, 20 Apr 2026 23:03:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8680fed5217e07032ae763bb4814082de2b6871eea99f7bcf4be6fb17dfd79f4`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 502.1 KB (502095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542cbb5df10cc920a089a68af1d0f860484ef70c9d225a612dcf5ada2aaef390`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88dd0729e80918b82e555dffd716238e73e864506f572bbbd0a8d756ec675bf`  
		Last Modified: Mon, 20 Apr 2026 23:03:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7176f52dbf05c4190cc72cf02fbe31e6539e8dcb732de302e9ebfd1e551f86`  
		Last Modified: Mon, 20 Apr 2026 23:03:47 GMT  
		Size: 20.2 MB (20193395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30381a09bd7e612f87bec4de2b1d777841f1d46d5ba73d38f9cced6f9b8115e4`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210f368239bd3baeaccf30803eaeec62843562f847f4f963141670c760522e87`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806603dc9170bc3b136c2941f1e2a772ccfaa85ee9aef9c22b08a74e983edb3e`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ec0ed78a357c0c8f98fc6487d30563e9d8a03db4def9807966493cbf91e4ec`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 23.4 MB (23434006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3950ad53b54530338b85e919a0e803046bdb1e51c7437915640748a7a11e53`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab184fdff530ee113fb07a551306f51ac338c1ac6d707c5e5ada12e7f3a9c3`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0306647508616ca419bbaf30c1bc7c5cb266e7dacac4b59856274b4243e01`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d91cba3e753e1dc5b702a3c5be5695fcc7d24a8cd552f8c620fb10598c4cbb3`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 11.9 MB (11925928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fccccf96f59c1b8f28e7403434c83676fd2918545b80fc004f6813a8b97e16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull docker@sha256:4d51f373dd2a4426a1fe2dc4967a42e90a0a2c22216d9f68feffdc36302b2e1a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2126278412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8971f266b87258d9fea7ed23e99b1644fc2244c0e02ad6d1188812c524886f54`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Mon, 20 Apr 2026 23:03:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:03:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:03:10 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:03:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:03:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:19 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:03:20 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:03:21 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:03:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:03:29 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:03:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:03:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f4559ccd19990eeb3eb464a5c03f7c8bd4e42fc037cc850c7dc5d79bf1767`  
		Last Modified: Mon, 20 Apr 2026 23:03:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8680fed5217e07032ae763bb4814082de2b6871eea99f7bcf4be6fb17dfd79f4`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 502.1 KB (502095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542cbb5df10cc920a089a68af1d0f860484ef70c9d225a612dcf5ada2aaef390`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88dd0729e80918b82e555dffd716238e73e864506f572bbbd0a8d756ec675bf`  
		Last Modified: Mon, 20 Apr 2026 23:03:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7176f52dbf05c4190cc72cf02fbe31e6539e8dcb732de302e9ebfd1e551f86`  
		Last Modified: Mon, 20 Apr 2026 23:03:47 GMT  
		Size: 20.2 MB (20193395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30381a09bd7e612f87bec4de2b1d777841f1d46d5ba73d38f9cced6f9b8115e4`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210f368239bd3baeaccf30803eaeec62843562f847f4f963141670c760522e87`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806603dc9170bc3b136c2941f1e2a772ccfaa85ee9aef9c22b08a74e983edb3e`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ec0ed78a357c0c8f98fc6487d30563e9d8a03db4def9807966493cbf91e4ec`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 23.4 MB (23434006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3950ad53b54530338b85e919a0e803046bdb1e51c7437915640748a7a11e53`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab184fdff530ee113fb07a551306f51ac338c1ac6d707c5e5ada12e7f3a9c3`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0306647508616ca419bbaf30c1bc7c5cb266e7dacac4b59856274b4243e01`  
		Last Modified: Mon, 20 Apr 2026 23:03:41 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d91cba3e753e1dc5b702a3c5be5695fcc7d24a8cd552f8c620fb10598c4cbb3`  
		Last Modified: Mon, 20 Apr 2026 23:03:43 GMT  
		Size: 11.9 MB (11925928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a0feb5c2dc7af77280683db28790048cd51f28ee9b61decefbe13a0518c9f308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull docker@sha256:93470c750610123e91ad43f5b232a408d9ddd6f4bea2355e23cf1996338a8c6e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186012082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa0979c8bbd379ec0dbae2915024f4ffde2fac2bcc3ba3b496f98c9b7bd3619`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Mon, 20 Apr 2026 23:07:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 20 Apr 2026 23:08:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 20 Apr 2026 23:08:29 GMT
ENV DOCKER_VERSION=29.4.1
# Mon, 20 Apr 2026 23:08:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.1.zip
# Mon, 20 Apr 2026 23:08:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:46 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Mon, 20 Apr 2026 23:08:47 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Mon, 20 Apr 2026 23:08:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 20 Apr 2026 23:08:56 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.3
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.3/docker-compose-windows-x86_64.exe
# Mon, 20 Apr 2026 23:08:57 GMT
ENV DOCKER_COMPOSE_SHA256=5e6d72612b3165be9fea4ae889435fec76979a9779b6f62f4efee99dd5f41ea1
# Mon, 20 Apr 2026 23:09:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdee3346b7a1b8ad53c9f8e5dd67903ff39beed2f224ac303b25f0dd869f8a8`  
		Last Modified: Mon, 20 Apr 2026 23:09:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa8f0463cf87863a82f8ca46c43dff6bfb2f9c87c13e93e06a6edd06c8b750`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 392.9 KB (392898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e18e138890e699b9b5d99167d6b27fba994d9215245cf671cf458b914e80877`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be321bf183f8a2f10257190607eee8f56ce000584dd762b27ce3518aebcc57fd`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acb94579e4a585da2995f4c9787e7e2a2bee991b0b32c72eabf497dd36fb452`  
		Last Modified: Mon, 20 Apr 2026 23:09:14 GMT  
		Size: 20.2 MB (20220932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77aed2b62f8dd25c6be38e3fab5b46266ebd4ea2997b3437c06d36df68fc52c`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3945a4a16522815c54613deb3d808ad5ead8f16aa81603d6abdaa24d3caba0da`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd670aa50e1a72277d3f64bb529f8c0c1b405016c951110ae6f38570d5a8e4f`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5231b475a9275d70c088ebeecd6c9c3fe1700aafc69aa1eb188bd3e3eb742a`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 23.5 MB (23452047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64155924f9009116e3d6e06e79a288000b5a370295cdae5f1d4c5fd0d249f974`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6488e27ba116d2e5753a6d7fc5fbcbab91a276c9048ebf533faa451482c0f70f`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799118bde74799785bee06618b18600a4d780d4cd28f0dddb41d4f4d6242ec8`  
		Last Modified: Mon, 20 Apr 2026 23:09:08 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ae9d5a1287309adeabaa8d5df55128ddc09f4c801edd7f13578c07590ed96`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 11.9 MB (11948368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

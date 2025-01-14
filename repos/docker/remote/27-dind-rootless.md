## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:aabc5074bcf4c93db6ea51fddba4983ea5ae72421b5a739fae19fc5fcee5e82c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:9a103862e4648fbcaf52c07bb8ef33db59ee46cbc1eedbc4cbdd10fc4af9788e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156158115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d95700034e28d044add69f30a925b41f26152ee4130b7e8081ca8bda098f95`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_VERSION=27.5.0
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.3
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-x86_64'; 			sha256='6ef48e4bf25fbf1f1ad50c43b797cc24e12e4cde29765076b4145e09e35f5713'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv6'; 			sha256='8f415a76ad62ff621b26b37a94841ee0d4480862d8da55320c1c8fc9db4d8359'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-armv7'; 			sha256='64314c73a7d34e4a8b9dad87bab857304fb60b0293703d02be436893e1c37f33'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-aarch64'; 			sha256='d1a04a3eb7fd738cc78e518d179a03adb9fe531ee422b8a14bdccf36d654b73a'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-ppc64le'; 			sha256='23bddc8119bce6c0eeef1461bc0526291d60de9042b28780012033ba4082090e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-riscv64'; 			sha256='c4bac574a2123938de4ef410e7cef92d079abe266298c93257cbcc4e17134184'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.3/docker-compose-linux-s390x'; 			sha256='6c0c7d9b6119f68b3dcbf816cf9e5782eb7cea8d2433f8a51b95a41276241e18'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD ["sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/var/lib/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 13 Jan 2025 22:12:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 13 Jan 2025 22:12:41 GMT
CMD []
# Mon, 13 Jan 2025 22:12:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.5.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.5.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 13 Jan 2025 22:12:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 13 Jan 2025 22:12:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2147a509bdeadcb92898e60247f4658852a925a4962e0e29a2d28fcfe83e81`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 8.1 MB (8058755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386023837c56d9b33f3b3c560d987a4d0afffaa2025b6bdb05dbb812ba5fd84d`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ec2a25f188dfb7b2d0d15b2f51239ab8694502bca535fd3c2ceccb359fd868`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18849469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c11d47744bce1446bbff20430a7058587389836041cbda659967ba94b3653`  
		Last Modified: Tue, 14 Jan 2025 01:33:35 GMT  
		Size: 18.8 MB (18798855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e324137ff7d6aef2c4fe2746097ee8c2ccfc69735be66123a60f1d9286e99c`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 19.3 MB (19303637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae739ff5a469e4fc30b28a279acac08ee7a9c6f40cee72753bf1cde14f2ea88`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c082b27e013c5d92e5f5698a5eb8564358982c6a8fcd01667c5e16e05499363`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1341245cb0ac938576ee4968bde808b58406e6dc5bad00b169e1584bd79a37`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ede50c7df8b73c8a3ac91fb3bb36978c76e031bb46b82aa12fa72fada06402`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 6.7 MB (6733496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285c3782350dd5f9e9ba3ffdca6909b3a357f12e4e0aa69f6509f071fbcfbe3`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23e2f46c920045fd9af6784bbff05014d36f9150a63b66c744172d76be81c4`  
		Last Modified: Tue, 14 Jan 2025 02:16:00 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dca5dcdd0a1de285b0723f6c07453eb8ad4c4e39c1d4685a5921590a3228e6`  
		Last Modified: Tue, 14 Jan 2025 02:16:02 GMT  
		Size: 58.4 MB (58383043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88a905ff3d6fd8eeb1a0e9a4da76911f3121664e953d721c866942a7926851a`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76253b0cea165b9074f6b67ca91b09076bb938e59f417391480e5db39bdf1a9`  
		Last Modified: Tue, 14 Jan 2025 02:16:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f935cb48b813bca67e3f4262bc998f10d445daf1ae1c2fe167bea1c7063459`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 986.6 KB (986564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a49473459905f4e8055629a7c6a93f3cef28430740f4a7460d66c31cebe219`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725ab53ec019a57158824c067b8d7c5d4aac14cac54bd82d929c6b3643929400`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a04e34cc60c0c247d0c4340ff8367878b45b1d4eb32445d48706d1c75078bab`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 21.3 MB (21303868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07647e8159772a3be30c90e3f36bcc2cc9575cd8e107a75a5dd202b40e50ec84`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f2bac0bc675c790fd6442f9801b8e048cf22f413d496faaac7d7d98f65e8775f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a58d67e13b913de17a6cef81562735d1cd54b387aeb9bd8393ebedaee21bac8`

```dockerfile
```

-	Layers:
	-	`sha256:9e2e64133b433d854e70c47e94e568307f6e6a9d22ba7f98ac3e92a3860b6b70`  
		Last Modified: Tue, 14 Jan 2025 03:17:21 GMT  
		Size: 30.6 KB (30617 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8877919584cc9a4577906c6c60656e7c44b7c8dae3b65f8d7b74acd9b8947ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149440959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b3ab72d35f78cfb25f15813532542dc016c0f9fd7889844e68ba6df769a39b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 18 Dec 2024 12:04:25 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_VERSION=27.4.1
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD ["sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.4.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.4.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/var/lib/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 18 Dec 2024 12:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 18 Dec 2024 12:04:25 GMT
CMD []
# Wed, 18 Dec 2024 12:04:25 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.4.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.4.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 18 Dec 2024 12:04:25 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 18 Dec 2024 12:04:25 GMT
USER rootless
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3528552267cec0f9e2dee7d372df3bbea6255a3ca1a18ba3e58e5cfd106d15e1`  
		Last Modified: Thu, 09 Jan 2025 22:29:23 GMT  
		Size: 8.1 MB (8073134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4781719ef357b2c136f17ff57b79d601b4058a8861d68048cf902106cf3ae9d`  
		Last Modified: Thu, 09 Jan 2025 22:29:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4866b03f4ce1c603a6809790707aae8972781d4ff1b1090b3960153b3abec1e0`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.6 MB (17619398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d036bb2a7049761d033d283b4bc752d8e2d6e25b9ea4bf4329e6a7055ad82e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.1 MB (17106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4fa20503c91c2405741c5b1d40f5567a7c641a4624b6c0693716eb0fa6752e`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 17.7 MB (17653961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f999290013a7bee6f7b09186deee9dc98564604594aac128b7293ef882edfd34`  
		Last Modified: Thu, 09 Jan 2025 22:29:42 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dca40438acce378f07676329455acd2969680d9ceeeee33d5f34cb1f06c2f4`  
		Last Modified: Thu, 09 Jan 2025 22:29:43 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c1436b4a8c8addd307436381ccbe5d3d3adf57e2b67228ea624046c0f4997`  
		Last Modified: Thu, 09 Jan 2025 22:29:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aed778d4d37e95ff4fef9353934ac33be3d14475532284512418c3c7e8802ea`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 7.0 MB (6981951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2357ac4e3b4ca2ae4efd996c265963976e946d8abe41868260f6fc228d6e6cc4`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 97.8 KB (97785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f2dd98d7754adf87dda19dcbdb3a884046d0c27693b4d9c3465c4ae77eca5c`  
		Last Modified: Thu, 09 Jan 2025 23:09:57 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af42edc6d44256189864a2f5cf56c06590a42e61aeb9f18a2c453de7841076b0`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 53.7 MB (53737271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ad24d587855579d9d75a11a4e2b7e0c347114c536d13580a4ea61bde47f9`  
		Last Modified: Thu, 09 Jan 2025 23:09:58 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbdc874d308be16b20915161093ad9bf64226aace0cc1e4a6c39989bc8b42e8`  
		Last Modified: Thu, 09 Jan 2025 23:09:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fb49e0358a6dcd8f454c229f2e58043c238bd1c31bf2592d90ccf2c54f4e51`  
		Last Modified: Fri, 10 Jan 2025 00:07:30 GMT  
		Size: 1.0 MB (1014210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439b04567bec34e568e7ccb361a72f63a1d46f4d92ecb655b923adc811884224`  
		Last Modified: Fri, 10 Jan 2025 00:07:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c5eaa7edf15934269fdc326ef1f67b1143f22258e44663c95398675d41f63`  
		Last Modified: Fri, 10 Jan 2025 00:07:29 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b68b3535056a1cc8be40c353f77739f156a5090082cc6be776be14d05d2caa1`  
		Last Modified: Fri, 10 Jan 2025 00:07:30 GMT  
		Size: 23.2 MB (23155143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f44128077eafee533110d4ac4367e5385cabd2739d3546d5c3d1dec4178ae04`  
		Last Modified: Fri, 10 Jan 2025 00:07:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3f6f181021a43b59a102e93c0b8ef6e94e8d5f579a9cfc058dccda16ea356cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fb060b226c196a27de2c0ef71eb8106443bf7c6124ee1de21d08359d8fb72d`

```dockerfile
```

-	Layers:
	-	`sha256:254aaf99f8db72b2d239c240a4ed5a914197c55e50a316ddee0c09a4ba50cfe8`  
		Last Modified: Fri, 10 Jan 2025 00:07:29 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

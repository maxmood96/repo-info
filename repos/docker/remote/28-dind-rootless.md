## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:607d248e893dc10308b8f70afad4bf26cf166836856284c00c9971ec9d9e7dc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:da8fe371cac264fe2cd720113802f7927e22a7c18ca08a3278a84339ad6470fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159355707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77bf29996b5bcf3e686137abea06877d76b39cfb63aff43fbdac12437fd8bd2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfbaa8510b4a4d47187d43cfb336caf2d7fc80ab68d68a803530b3b4d906633`  
		Last Modified: Thu, 10 Apr 2025 18:53:49 GMT  
		Size: 8.1 MB (8062935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42a0bc42a48d8fa397968f3dc30205c3d52f95e8fc9edf44ff00db95e3196e1`  
		Last Modified: Thu, 10 Apr 2025 18:53:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cd23755334f4438da6db977b2e3c8eb151b552407089a101aa9d2ec97144fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:49 GMT  
		Size: 19.5 MB (19543064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5138e6e2c82165771dfb34e1de33084bd4407f686a179c99643373b5aaaec47a`  
		Last Modified: Thu, 10 Apr 2025 18:53:49 GMT  
		Size: 21.8 MB (21848955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8eee1d6b74eec22288a615bf3bedebc10e1386e8fbf9c4619b3a541f843c56`  
		Last Modified: Thu, 10 Apr 2025 18:53:50 GMT  
		Size: 20.9 MB (20915264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1831b367f0bd1545076fc7359eaffc1566af6b06259d80b1b432e642e3c5f79e`  
		Last Modified: Thu, 10 Apr 2025 18:53:50 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f40a918875389f0d981288b783b22dcf9b224f1142a6ea3cf951b1a280ba722`  
		Last Modified: Thu, 10 Apr 2025 18:53:51 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1260a011c8704fd735d02d4d447b37146aa14ee72c77ab65de9643c835619248`  
		Last Modified: Thu, 10 Apr 2025 18:53:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57686a87e5062e9e0e7e3e0633ce64e40fc9a22ea5d7e643bca819afdcb884b6`  
		Last Modified: Thu, 10 Apr 2025 19:01:37 GMT  
		Size: 6.7 MB (6732980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a4c88b1330f0e1bcc282900610e068e3f188e0c5e2d3144e152e9d543914b7`  
		Last Modified: Thu, 10 Apr 2025 19:01:37 GMT  
		Size: 90.3 KB (90331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc577e801c9b7ee427b8c63341557ffec0e21897f9e2e0695a03bc4eea91ae26`  
		Last Modified: Thu, 10 Apr 2025 19:01:36 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aad24c5254211f256ea8d5375c14040846a9680f16ef01067bc5766fd22242a`  
		Last Modified: Thu, 10 Apr 2025 19:01:38 GMT  
		Size: 60.4 MB (60352737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4964c8f3f5e0abd33a72b7476538cf95bc36a22fbd3d8086644954e5b1abb6d`  
		Last Modified: Thu, 10 Apr 2025 19:01:38 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b17c6a5a7a377776b1308641056d468a2e2a3c4889b066726b8cd245e3873e7`  
		Last Modified: Thu, 10 Apr 2025 19:01:38 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec4b1e3bff50ad0851b830cfc73e70d7efd818fc62961be7ec3e299b2853a3b`  
		Last Modified: Thu, 10 Apr 2025 19:07:47 GMT  
		Size: 986.6 KB (986581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651896a1bcecdeae952962fc763353100874322bd4d537e974b110e64014c9f7`  
		Last Modified: Thu, 10 Apr 2025 19:07:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14a049cde99729d312de96626c2a498a027ab9e1911efc0a94568df464cd7da`  
		Last Modified: Thu, 10 Apr 2025 19:07:47 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3632364a49621e28a36ff963193aed57006f23e4103b38138465025fc477bcbb`  
		Last Modified: Thu, 10 Apr 2025 19:07:48 GMT  
		Size: 17.2 MB (17171162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22ad8b45781c9bbb8bbd03262c1850be6ddc3e95b75b2896b9c42c142fd795b`  
		Last Modified: Thu, 10 Apr 2025 19:07:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0fc572b5b704f427119df61e6326149ad5f96617c4b429ac58305fc66b271bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb68da6e1e0ae0973626da64db51db08408c105aaeb39dfb004c73a52ef6373c`

```dockerfile
```

-	Layers:
	-	`sha256:22bc8e7ba6dae3dcebc2add94e28269aea2c2610dcc6b1b1efb3dcc79d829478`  
		Last Modified: Thu, 10 Apr 2025 19:07:47 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9672188de5af899f6a0832b9286f6571ca3149f82106b25e386812e4cf80b54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152849175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f046f51cd072b1ec0105c4c2bf6f2410db72b4a5beaf2663aa97973d8e8f97b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD ["sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Mar 2025 17:04:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Mar 2025 17:04:17 GMT
CMD []
# Tue, 25 Mar 2025 17:04:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Mar 2025 17:04:17 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Mar 2025 17:04:17 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd5ff2c8ce32662254aec1f5895335944c0a1091ad370582654c941020837f6`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 8.1 MB (8077244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05954605b1b02bfb30cf5be89670899670e3afb9c38d5a64b6ba2d8a0c85f1a3`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b2d5601b209a8377462fbeb8584639083f2a1b6cb0e787aecc0cf6ef535a97`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 18.5 MB (18457148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafcef0b27a201db6e875c0d98c7b89fc6d905270107422298feb6dca964f128`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.1 MB (20061183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babd1bd7a49dd018bb3f90d4dc8258e8a3ed64107e131486ce4761fbfa7ce840`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.2 MB (19165689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5841602211e27b82ad14c42542ac326d4de75902e0629504f6c434ded641c7db`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cd8ae263d27b39614fe039584e0cf8f7a4f5db1f348cb9188127ef1465ff14`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6c1804a175a38353da82bc6258e57d9f7b6f76a2b9e322636f691608020941`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b95c7b26e51e777d0c5730cbc2520b02bf70c620f212ac20e54f97ff29ab2`  
		Last Modified: Thu, 10 Apr 2025 19:00:51 GMT  
		Size: 7.0 MB (6978832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d578234151192d09fb86781bda264c9a84e90556d73f6f739225703660e18c`  
		Last Modified: Thu, 10 Apr 2025 19:00:51 GMT  
		Size: 99.4 KB (99388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a11a42c75ff8d7277c84835475697bdee3935726871b39c153ae8dfad19823`  
		Last Modified: Thu, 10 Apr 2025 19:00:51 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7db168e2e821ff818ae58607e66ddceda9a236e94971e909b6326d377838bad`  
		Last Modified: Thu, 10 Apr 2025 19:00:53 GMT  
		Size: 55.7 MB (55710878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8ed069fdff956fe57c5978f1c66e1687edc4d88bacb365cea45e39e47dad77`  
		Last Modified: Thu, 10 Apr 2025 19:00:52 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bbc05962c373ee24e9cbd3f6a2ad42877c0c19426b8ded0696fc2041c8267d`  
		Last Modified: Thu, 10 Apr 2025 19:00:52 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad78b8bc8ca5b9360ecbdc60a415b5da9ad69c231a06563b453ab1564c52252`  
		Last Modified: Thu, 10 Apr 2025 19:25:32 GMT  
		Size: 1.0 MB (1014199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6d542e963dfd216dafa9d6dfd0e3ebe4a30ff795a3214b69fc3c13a5381214`  
		Last Modified: Thu, 10 Apr 2025 19:25:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995b3fef175d17ed4fecb7fce79af763f79ea078fdba0b15d1e1e1a9581f5529`  
		Last Modified: Thu, 10 Apr 2025 19:25:27 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd38970b0d1afaac534cb10d8161e81095bbd3e59343770ddf76d60b55c9859`  
		Last Modified: Thu, 10 Apr 2025 19:25:28 GMT  
		Size: 19.3 MB (19282132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7ae8d3f54a7f598ae4cb83c01fde0d78371964b3fffdb46045a1e9375b4a47`  
		Last Modified: Thu, 10 Apr 2025 19:25:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e3807fedf6f687fb387e2e4108100ff4158dd6e199de23ebc45a96acb814af0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a030f63ed0d96ebcf0f852aa09e285f5be72f5345f12ef0978453f0b19a1275a`

```dockerfile
```

-	Layers:
	-	`sha256:174e6908692f5e399ab33dd4e79d77a30b8488db363a108bd8c7a1e3043a2b5b`  
		Last Modified: Thu, 10 Apr 2025 19:25:26 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

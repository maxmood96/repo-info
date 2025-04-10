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
-	[`docker:28.0.4`](#docker2804)
-	[`docker:28.0.4-alpine3.21`](#docker2804-alpine321)
-	[`docker:28.0.4-cli`](#docker2804-cli)
-	[`docker:28.0.4-cli-alpine3.21`](#docker2804-cli-alpine321)
-	[`docker:28.0.4-dind`](#docker2804-dind)
-	[`docker:28.0.4-dind-alpine3.21`](#docker2804-dind-alpine321)
-	[`docker:28.0.4-dind-rootless`](#docker2804-dind-rootless)
-	[`docker:28.0.4-windowsservercore`](#docker2804-windowsservercore)
-	[`docker:28.0.4-windowsservercore-1809`](#docker2804-windowsservercore-1809)
-	[`docker:28.0.4-windowsservercore-ltsc2022`](#docker2804-windowsservercore-ltsc2022)
-	[`docker:28.0.4-windowsservercore-ltsc2025`](#docker2804-windowsservercore-ltsc2025)
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
$ docker pull docker@sha256:ddb0033088b4fab74881ade341a582e3c6c8021b82377703ba1a6106bd3ded44
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
$ docker pull docker@sha256:39c7ad73456a07cc38f6201542bb8fe90af7011bbfdeedd1a38d4073f231eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141196623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915daf53f2101bf4d33fd02a660d3380b7ae93c33353b8e89d490f88d99fe063`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:6fd9637e488f1aeddf77f0350669aab55ef3ba8513096467f7fdda49319b6aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c39104ed185c00634458eb4ac944cc4e3573157117d83049d13e426a8d9c82b`

```dockerfile
```

-	Layers:
	-	`sha256:d426f1591ec7aba06d77dfe270fc9e4bdf14a45b0dffdd3cc2e01d164c846f26`  
		Last Modified: Thu, 10 Apr 2025 19:01:36 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:f57bfe085889a95865995e69923b8c2d367e85ce52c02e8a7104749a580824ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131831229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0574bca6d6758ad673efce2f9b025494e66ba0f910eaa2d6b6595a8e4f6358b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2be501a51d4a1f0a576d79fbe13fe078b4bdbf776ed23cf879526ede3ef5e1`  
		Last Modified: Thu, 10 Apr 2025 19:00:55 GMT  
		Size: 7.0 MB (7036868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63997f7b0bbee48aec78071d1b0c603d44f66f2ea8b8d94000c1ecaf1c6104`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 89.9 KB (89861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7912ed8760d96518614159b4b19b70b895740d64c6f5fd05d096b33364737`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd81cb731158170a092369d294fde221053b50d8bbc81edbf3e97d07bc1fbb`  
		Last Modified: Thu, 10 Apr 2025 19:00:57 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb345ef49ff2d099926b4b83939cfa58a3a46fb13ba97090b378e589e8b520`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db539f3ab5ee441f7079488bcfebcbea706e544d414404b94bdbeb9346e2dfe`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:cbd722e549eb223a43ea7d493ead3354c85f66568db49c81d21988c69328147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dff5dcf2da2754b63daf44a1ef2835e410f441cd331f7acf9f2e7e2b5b87652`

```dockerfile
```

-	Layers:
	-	`sha256:378ab517d099321cd0621b9b29b751a08fefaa9b86368894c6a55e150d700860`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:1301cf6f282edbc7d94f178d2c0eec8394d27ef4583d71f8de15d7f3dd95dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130168775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a9103d3f83801d92a29c64c17850d951bec8b8d8ff10649c9ab13809b0a5a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aad6696717cc1615cc26f88fcafdff76f694a30eb5acf705c8363975f1e651`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 6.4 MB (6366036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245fa4cf98e8dd69566bc3e134d2fac91668df09f86fdcac3355d6694aa6191c`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 86.4 KB (86355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3167df5245a23cda38488a5fe3f8e58eb4176fb82896f6995ef46c98970c9`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f510c9deee4bcd5c38974dc46e0017e99e4725922e6e4946049c7d7107a47a`  
		Last Modified: Thu, 10 Apr 2025 19:00:48 GMT  
		Size: 55.7 MB (55741207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7919e15335d560caec91132a82a0dcc2d10952d51a073120aa793accc2651f`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24e3806a3f99ba66384d8e146985e86018b9652e0c3b7d6d6773fd939fda0b`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:7265de37982ade6cf359e6c152e6c05c89d4139cd11fcb5cf319ebc88b42497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8f79d22adc370d29acb203ab10dfe28d735a51e4ba15c1b1cbaae93c747b9b`

```dockerfile
```

-	Layers:
	-	`sha256:279933e04881d0f9dd131077fec7e0243e4fb68bd92873e62fa6b7791b84d285`  
		Last Modified: Thu, 10 Apr 2025 19:00:45 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7758019ffa34f3badc161535e37606309d838fe5dc8774ff95c6f8d03371be53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132551502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6bae33c1f057ecfe982e5da8ac6862fb24634b9f314179501611fb2812e53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:e6c2bff16952f87dbf0660cbc7e3b894101e54070b72fe08f5ad6760ee0fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab359cbfa98deb3b443cef392d6076cd9cae3a5f443641500ac380c6c81ffe17`

```dockerfile
```

-	Layers:
	-	`sha256:466b4a3f5e33095850c5458dc8e94c486cb9cc628b450c8e203cd9d5fb180aae`  
		Last Modified: Thu, 10 Apr 2025 19:00:50 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:db3ecdf8e404584aa9c61124d4b94050a57baff6b22b6c24fd4306ba2ec0ee7f
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
$ docker pull docker@sha256:a6ea1ff707f785adb9be2f6e47e87700acf25028f2d9967d13b76431ea6df122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74014617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0289ff325f81264fd1a632fff7b28d944ff609ba51d8209663b51d4cbd458f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6169c645a49b492d6e68d672c3d1a916c2a8e4dd3c202c56fab0c1d2be6faaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ad129589ab4978d3da3e6ef2f6e3f4f5a0ac153762f2508d8f449b0a2ca999`

```dockerfile
```

-	Layers:
	-	`sha256:8c1f247b52e1e0f2bed9ae6eabd4518ca193f0085972b55c7d23a8898a174d70`  
		Last Modified: Thu, 10 Apr 2025 18:53:49 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:14eff0079ba0251493cf5982ca5b686ca7e1593b4e2cbb96c60123f917fe8d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68957297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b7b4e4a140075fe07f7d66321e2a97fdd546d69a162a7be5bc94d5798a42dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4fb6114e207be2cba4b2c019acb8be57897e196a2e6f4dc5d987772c0b43eaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab926911105f673368ef7c6dc6b1867f1ec4adcf7e3c4945ce3c1672996fd7fd`

```dockerfile
```

-	Layers:
	-	`sha256:ed38fd2f67937dcec97c17b94519db624b47e1988d2bbbd46b9f48eac203ad8b`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:12b3a15f36a8eb6cc92894f64cb1b50a6803355bc5304a3bd83dcc90bf5ad495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67969222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e080826ce1b653f01b7fb18b04d27924f0224e0be29ad901b75a2970050ca7b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4afba38ec0f337734749f2c8b49e227a3d45f9f61389dbd68c9e7eecac222c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e89b56991dd0c0c1c8cbb2d9a7a7dc416f9f9f6b25120f4876559ffdb18d9`

```dockerfile
```

-	Layers:
	-	`sha256:279111cff860bea667d5c8682bb1a01b5bc0faf6cc7efd773554b9c7a12570c2`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:950fa733cdc541a5eaf180844e947417d625e7f1a5c2c2b11d739df98b7d0f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69756446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f62597355eb100013cdc808e76630be3420f850178b0bc0d90967c71a1c0852`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
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

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:39fd6f38aadc7c0729162941c92ea691ecabb023e6d976d71ceb673074ac230c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6643e2ca409745126713435320e0adac8ab3601ef2e01b647418f12ff740aea`

```dockerfile
```

-	Layers:
	-	`sha256:0640e53e70ef0e3d76844ae18c7b1d4b97d228264c700bcd5125ddfbd7443360`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:ddb0033088b4fab74881ade341a582e3c6c8021b82377703ba1a6106bd3ded44
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
$ docker pull docker@sha256:39c7ad73456a07cc38f6201542bb8fe90af7011bbfdeedd1a38d4073f231eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141196623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915daf53f2101bf4d33fd02a660d3380b7ae93c33353b8e89d490f88d99fe063`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6fd9637e488f1aeddf77f0350669aab55ef3ba8513096467f7fdda49319b6aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c39104ed185c00634458eb4ac944cc4e3573157117d83049d13e426a8d9c82b`

```dockerfile
```

-	Layers:
	-	`sha256:d426f1591ec7aba06d77dfe270fc9e4bdf14a45b0dffdd3cc2e01d164c846f26`  
		Last Modified: Thu, 10 Apr 2025 19:01:36 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f57bfe085889a95865995e69923b8c2d367e85ce52c02e8a7104749a580824ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131831229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0574bca6d6758ad673efce2f9b025494e66ba0f910eaa2d6b6595a8e4f6358b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2be501a51d4a1f0a576d79fbe13fe078b4bdbf776ed23cf879526ede3ef5e1`  
		Last Modified: Thu, 10 Apr 2025 19:00:55 GMT  
		Size: 7.0 MB (7036868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63997f7b0bbee48aec78071d1b0c603d44f66f2ea8b8d94000c1ecaf1c6104`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 89.9 KB (89861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7912ed8760d96518614159b4b19b70b895740d64c6f5fd05d096b33364737`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd81cb731158170a092369d294fde221053b50d8bbc81edbf3e97d07bc1fbb`  
		Last Modified: Thu, 10 Apr 2025 19:00:57 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb345ef49ff2d099926b4b83939cfa58a3a46fb13ba97090b378e589e8b520`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db539f3ab5ee441f7079488bcfebcbea706e544d414404b94bdbeb9346e2dfe`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:cbd722e549eb223a43ea7d493ead3354c85f66568db49c81d21988c69328147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dff5dcf2da2754b63daf44a1ef2835e410f441cd331f7acf9f2e7e2b5b87652`

```dockerfile
```

-	Layers:
	-	`sha256:378ab517d099321cd0621b9b29b751a08fefaa9b86368894c6a55e150d700860`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:1301cf6f282edbc7d94f178d2c0eec8394d27ef4583d71f8de15d7f3dd95dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130168775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a9103d3f83801d92a29c64c17850d951bec8b8d8ff10649c9ab13809b0a5a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aad6696717cc1615cc26f88fcafdff76f694a30eb5acf705c8363975f1e651`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 6.4 MB (6366036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245fa4cf98e8dd69566bc3e134d2fac91668df09f86fdcac3355d6694aa6191c`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 86.4 KB (86355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3167df5245a23cda38488a5fe3f8e58eb4176fb82896f6995ef46c98970c9`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f510c9deee4bcd5c38974dc46e0017e99e4725922e6e4946049c7d7107a47a`  
		Last Modified: Thu, 10 Apr 2025 19:00:48 GMT  
		Size: 55.7 MB (55741207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7919e15335d560caec91132a82a0dcc2d10952d51a073120aa793accc2651f`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24e3806a3f99ba66384d8e146985e86018b9652e0c3b7d6d6773fd939fda0b`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:7265de37982ade6cf359e6c152e6c05c89d4139cd11fcb5cf319ebc88b42497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8f79d22adc370d29acb203ab10dfe28d735a51e4ba15c1b1cbaae93c747b9b`

```dockerfile
```

-	Layers:
	-	`sha256:279933e04881d0f9dd131077fec7e0243e4fb68bd92873e62fa6b7791b84d285`  
		Last Modified: Thu, 10 Apr 2025 19:00:45 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7758019ffa34f3badc161535e37606309d838fe5dc8774ff95c6f8d03371be53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132551502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6bae33c1f057ecfe982e5da8ac6862fb24634b9f314179501611fb2812e53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e6c2bff16952f87dbf0660cbc7e3b894101e54070b72fe08f5ad6760ee0fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab359cbfa98deb3b443cef392d6076cd9cae3a5f443641500ac380c6c81ffe17`

```dockerfile
```

-	Layers:
	-	`sha256:466b4a3f5e33095850c5458dc8e94c486cb9cc628b450c8e203cd9d5fb180aae`  
		Last Modified: Thu, 10 Apr 2025 19:00:50 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

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

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:b4976a3b828001015b15b82f7164b772b541d63c40ff57d25001d0a654e09e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8084d47f9c866ffb0fc6c74d818412ff1196f96066e4460f40ddb325112e0dcc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3460019679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8eb0a28181dcd66cffe910466b7bc06081957269945180b9e3be0f83af31bd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:39:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:39:26 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:39:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:39:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:39:39 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:39:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:39:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:39:50 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:39:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90663cbdd92914b16d1b360ec39197f6848f810c2e3d5f75368367b755fb29a5`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6859709f79778e74c7ef624e307d1930c0f780d10be536cb85d9893936b1d2`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 364.7 KB (364741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f3f9fb8993e6eddeb12b79a24923159ad4bba9c61def71fa12ee3f22eb949b`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b566c3c24e01288e140412f9834c019e4e2e71145ed6b6b079795f86b97424f2`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc5f946c4df03788d89b893a24b781d0bf21407cc2582ef5194f0eaea08db74`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 19.9 MB (19876882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2a3d26ad4275972b61ccdede64c0ddf0788bfa910b1275b74d172e5082198`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ad96060e962414395bc1991729228e8ca1e139d5b228efc120a55e2b9cab5`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb45857c62165be6ffbdcee3d0a6ae915dec7440305fc6ebfc274ca67879d0de`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946bf5bea56a89ae65bdacd4edde0517f360ff8ebcabd76df02411213a273c01`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.8 MB (22779634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6100d6c301fb149b342ede708f60d3cb8e10a3c1e9e3836c1baf34221724cef0`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d08118b8b7f3b7ff9643a05fa0fabf35417f346904745264b1b7878d575e1d`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8922e187bf58aaae3a9c3e2e9e8cfb6b00b0ad16a4e8cd5a47b91da0443a6`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93978eb25ad6c40ce8eccddc334dfe92007d5cc7ed7df32eaef8dd97ec678442`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.3 MB (22307251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:0fe4c4d0f5c80021c50c85d104ea9454679f65eef396c515473415b2f3551677
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336245643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2260686200048a8ce26b4461ef2e6b0b73d9ce4353bad23921ebc2a3c91998b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:53:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:53:44 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:53:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:53:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:53:56 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:54:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:54:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:54:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd31ce4b72c969f090b09e0d47519bd245635b8a0766cad50a94e5285269e7f`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611d42417bb7b25c9cbe870a1d686b89d1d9756d80d42e4fd6e078d9f81ce4a`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 346.1 KB (346062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb06dc8ecf1b08f1190ad1c0d83e1fdabc1c8d67fc1ac6cb12116132b4f03468`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008480b629bc35e084765059b6f319dc7ff56f6ddd835cde71f710a1d1b3d636`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c50ac98d04810f7b347835e962e1cc758aeb4ba0ee8a7231139b95c1d2bde`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 19.9 MB (19852659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107085d17762a97b5dc8bd94314f73c5a529607173545e1afaca9a1d379c104d`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271fac6913f53452e4c148e110e15c1cf204cafbed62e7609172534dea68b05f`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c075328080e6995af18ba0d46caacfb2d481e3bfd03bd1e1feb30c92ef355`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff40e518cab6103cc2dbbed344e68095afb68f480c2690b74900f7a7412e1ae9`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 22.8 MB (22756339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a62709feb8f58e8269a332f8cb621fcd984c1c3316283ccded16919bf71cda`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6acbdb8f48fcce734907c9a41f60cd59f358e65c812a3a4981f5e8b3276d52e`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1edc9932a94ae1c328f7a4190d5780f481b8890967cbc0e915a092e9a8f0871`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececc62a636024315de22ccaac302436c36e77452a38b7f08b83dca6b0795455`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 22.3 MB (22283301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:fa94327469822a56e83053ec60f804486fe9ee64c9f15be87233d2651926c32b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227933081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffec676bac1f14cd20f776a437da6b9fe135a587eb81263ff81adc16bb644ca6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 01:19:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:19:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 01:19:53 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 01:19:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 01:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 01:20:09 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 01:20:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 01:20:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 01:20:20 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 01:20:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243c89dd211d21587050138b4ba9caca0157449d59d6698f399bda8c9ac09647`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a64f1cb97b9459857deaad35fc7cb3146d6d807da8b42954f5570e8015ff8d`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 331.8 KB (331794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1ff6cf58cfc4c73c2c1cb14b2dbd5e91ccd8342cf3e7b4979f8c273605063b`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e961a01ad0f71ba1051d35d21755803b2fa1951fba5c545b345c4ddb497d4cf`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba307589781f303a1e20fe2f5c8a65fe379191b2f06f8de840ea2aaecf184f47`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 19.8 MB (19844611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb7ebad4ed4801f9cb8c8b750ab2454c93c826a400f3e5ac972a921b43dd3f2`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55c409429d09b5ed5634e52d87d957962d25ed1cd4d0dd5b62783cd4e2f446`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd36acd6048ee7eb5e37f47ea0ed75fb4bbcc90983346c92ae7cc8a3a43aa0a`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4383de892731480789dbba3ea542e0493a181b4619b7feb20fdd1701337750`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.7 MB (22748533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7686b51d722ad3222e89104c832b025336bd4a4a7c2beb26fa7eb95875deafbd`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cb46454301b3cc3fcacd9a425240920b39672c040ac885da807dfc3a33746f`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e72a7a6e8ddcef11a9b230a1cec67389895ec62572710f439e53ed43a59c019`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88569070dd26d817476810a2cd6ad26ea8f4e775ccdf912cbf72eef0203286a`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.3 MB (22270587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:cc2efcf0a0bafa3c9df47a975aa3a6f095645104779c3b74fa0ff3ec9b2e1e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:fa94327469822a56e83053ec60f804486fe9ee64c9f15be87233d2651926c32b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227933081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffec676bac1f14cd20f776a437da6b9fe135a587eb81263ff81adc16bb644ca6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 01:19:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:19:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 01:19:53 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 01:19:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 01:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 01:20:09 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 01:20:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 01:20:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 01:20:20 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 01:20:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243c89dd211d21587050138b4ba9caca0157449d59d6698f399bda8c9ac09647`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a64f1cb97b9459857deaad35fc7cb3146d6d807da8b42954f5570e8015ff8d`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 331.8 KB (331794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1ff6cf58cfc4c73c2c1cb14b2dbd5e91ccd8342cf3e7b4979f8c273605063b`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e961a01ad0f71ba1051d35d21755803b2fa1951fba5c545b345c4ddb497d4cf`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba307589781f303a1e20fe2f5c8a65fe379191b2f06f8de840ea2aaecf184f47`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 19.8 MB (19844611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb7ebad4ed4801f9cb8c8b750ab2454c93c826a400f3e5ac972a921b43dd3f2`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55c409429d09b5ed5634e52d87d957962d25ed1cd4d0dd5b62783cd4e2f446`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd36acd6048ee7eb5e37f47ea0ed75fb4bbcc90983346c92ae7cc8a3a43aa0a`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4383de892731480789dbba3ea542e0493a181b4619b7feb20fdd1701337750`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.7 MB (22748533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7686b51d722ad3222e89104c832b025336bd4a4a7c2beb26fa7eb95875deafbd`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cb46454301b3cc3fcacd9a425240920b39672c040ac885da807dfc3a33746f`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e72a7a6e8ddcef11a9b230a1cec67389895ec62572710f439e53ed43a59c019`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88569070dd26d817476810a2cd6ad26ea8f4e775ccdf912cbf72eef0203286a`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.3 MB (22270587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fe87151fca5614738a9a2377a76c82a06dcd81fa4827ccffb171958d6fb8494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:0fe4c4d0f5c80021c50c85d104ea9454679f65eef396c515473415b2f3551677
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336245643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2260686200048a8ce26b4461ef2e6b0b73d9ce4353bad23921ebc2a3c91998b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:53:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:53:44 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:53:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:53:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:53:56 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:54:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:54:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:54:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd31ce4b72c969f090b09e0d47519bd245635b8a0766cad50a94e5285269e7f`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611d42417bb7b25c9cbe870a1d686b89d1d9756d80d42e4fd6e078d9f81ce4a`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 346.1 KB (346062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb06dc8ecf1b08f1190ad1c0d83e1fdabc1c8d67fc1ac6cb12116132b4f03468`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008480b629bc35e084765059b6f319dc7ff56f6ddd835cde71f710a1d1b3d636`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c50ac98d04810f7b347835e962e1cc758aeb4ba0ee8a7231139b95c1d2bde`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 19.9 MB (19852659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107085d17762a97b5dc8bd94314f73c5a529607173545e1afaca9a1d379c104d`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271fac6913f53452e4c148e110e15c1cf204cafbed62e7609172534dea68b05f`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c075328080e6995af18ba0d46caacfb2d481e3bfd03bd1e1feb30c92ef355`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff40e518cab6103cc2dbbed344e68095afb68f480c2690b74900f7a7412e1ae9`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 22.8 MB (22756339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a62709feb8f58e8269a332f8cb621fcd984c1c3316283ccded16919bf71cda`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6acbdb8f48fcce734907c9a41f60cd59f358e65c812a3a4981f5e8b3276d52e`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1edc9932a94ae1c328f7a4190d5780f481b8890967cbc0e915a092e9a8f0871`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececc62a636024315de22ccaac302436c36e77452a38b7f08b83dca6b0795455`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 22.3 MB (22283301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:7aacee74867dda438d28dbabea6db4a5d0891bc6ef5f0174dcd201910d0b3d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8084d47f9c866ffb0fc6c74d818412ff1196f96066e4460f40ddb325112e0dcc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3460019679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8eb0a28181dcd66cffe910466b7bc06081957269945180b9e3be0f83af31bd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:39:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:39:26 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:39:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:39:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:39:39 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:39:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:39:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:39:50 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:39:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90663cbdd92914b16d1b360ec39197f6848f810c2e3d5f75368367b755fb29a5`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6859709f79778e74c7ef624e307d1930c0f780d10be536cb85d9893936b1d2`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 364.7 KB (364741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f3f9fb8993e6eddeb12b79a24923159ad4bba9c61def71fa12ee3f22eb949b`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b566c3c24e01288e140412f9834c019e4e2e71145ed6b6b079795f86b97424f2`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc5f946c4df03788d89b893a24b781d0bf21407cc2582ef5194f0eaea08db74`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 19.9 MB (19876882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2a3d26ad4275972b61ccdede64c0ddf0788bfa910b1275b74d172e5082198`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ad96060e962414395bc1991729228e8ca1e139d5b228efc120a55e2b9cab5`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb45857c62165be6ffbdcee3d0a6ae915dec7440305fc6ebfc274ca67879d0de`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946bf5bea56a89ae65bdacd4edde0517f360ff8ebcabd76df02411213a273c01`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.8 MB (22779634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6100d6c301fb149b342ede708f60d3cb8e10a3c1e9e3836c1baf34221724cef0`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d08118b8b7f3b7ff9643a05fa0fabf35417f346904745264b1b7878d575e1d`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8922e187bf58aaae3a9c3e2e9e8cfb6b00b0ad16a4e8cd5a47b91da0443a6`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93978eb25ad6c40ce8eccddc334dfe92007d5cc7ed7df32eaef8dd97ec678442`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.3 MB (22307251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0`

```console
$ docker pull docker@sha256:ddb0033088b4fab74881ade341a582e3c6c8021b82377703ba1a6106bd3ded44
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
$ docker pull docker@sha256:39c7ad73456a07cc38f6201542bb8fe90af7011bbfdeedd1a38d4073f231eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141196623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915daf53f2101bf4d33fd02a660d3380b7ae93c33353b8e89d490f88d99fe063`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:6fd9637e488f1aeddf77f0350669aab55ef3ba8513096467f7fdda49319b6aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c39104ed185c00634458eb4ac944cc4e3573157117d83049d13e426a8d9c82b`

```dockerfile
```

-	Layers:
	-	`sha256:d426f1591ec7aba06d77dfe270fc9e4bdf14a45b0dffdd3cc2e01d164c846f26`  
		Last Modified: Thu, 10 Apr 2025 19:01:36 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:f57bfe085889a95865995e69923b8c2d367e85ce52c02e8a7104749a580824ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131831229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0574bca6d6758ad673efce2f9b025494e66ba0f910eaa2d6b6595a8e4f6358b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2be501a51d4a1f0a576d79fbe13fe078b4bdbf776ed23cf879526ede3ef5e1`  
		Last Modified: Thu, 10 Apr 2025 19:00:55 GMT  
		Size: 7.0 MB (7036868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63997f7b0bbee48aec78071d1b0c603d44f66f2ea8b8d94000c1ecaf1c6104`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 89.9 KB (89861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7912ed8760d96518614159b4b19b70b895740d64c6f5fd05d096b33364737`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd81cb731158170a092369d294fde221053b50d8bbc81edbf3e97d07bc1fbb`  
		Last Modified: Thu, 10 Apr 2025 19:00:57 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb345ef49ff2d099926b4b83939cfa58a3a46fb13ba97090b378e589e8b520`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db539f3ab5ee441f7079488bcfebcbea706e544d414404b94bdbeb9346e2dfe`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:cbd722e549eb223a43ea7d493ead3354c85f66568db49c81d21988c69328147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dff5dcf2da2754b63daf44a1ef2835e410f441cd331f7acf9f2e7e2b5b87652`

```dockerfile
```

-	Layers:
	-	`sha256:378ab517d099321cd0621b9b29b751a08fefaa9b86368894c6a55e150d700860`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:1301cf6f282edbc7d94f178d2c0eec8394d27ef4583d71f8de15d7f3dd95dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130168775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a9103d3f83801d92a29c64c17850d951bec8b8d8ff10649c9ab13809b0a5a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aad6696717cc1615cc26f88fcafdff76f694a30eb5acf705c8363975f1e651`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 6.4 MB (6366036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245fa4cf98e8dd69566bc3e134d2fac91668df09f86fdcac3355d6694aa6191c`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 86.4 KB (86355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3167df5245a23cda38488a5fe3f8e58eb4176fb82896f6995ef46c98970c9`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f510c9deee4bcd5c38974dc46e0017e99e4725922e6e4946049c7d7107a47a`  
		Last Modified: Thu, 10 Apr 2025 19:00:48 GMT  
		Size: 55.7 MB (55741207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7919e15335d560caec91132a82a0dcc2d10952d51a073120aa793accc2651f`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24e3806a3f99ba66384d8e146985e86018b9652e0c3b7d6d6773fd939fda0b`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:7265de37982ade6cf359e6c152e6c05c89d4139cd11fcb5cf319ebc88b42497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8f79d22adc370d29acb203ab10dfe28d735a51e4ba15c1b1cbaae93c747b9b`

```dockerfile
```

-	Layers:
	-	`sha256:279933e04881d0f9dd131077fec7e0243e4fb68bd92873e62fa6b7791b84d285`  
		Last Modified: Thu, 10 Apr 2025 19:00:45 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7758019ffa34f3badc161535e37606309d838fe5dc8774ff95c6f8d03371be53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132551502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6bae33c1f057ecfe982e5da8ac6862fb24634b9f314179501611fb2812e53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0` - unknown; unknown

```console
$ docker pull docker@sha256:e6c2bff16952f87dbf0660cbc7e3b894101e54070b72fe08f5ad6760ee0fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab359cbfa98deb3b443cef392d6076cd9cae3a5f443641500ac380c6c81ffe17`

```dockerfile
```

-	Layers:
	-	`sha256:466b4a3f5e33095850c5458dc8e94c486cb9cc628b450c8e203cd9d5fb180aae`  
		Last Modified: Thu, 10 Apr 2025 19:00:50 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-cli`

```console
$ docker pull docker@sha256:db3ecdf8e404584aa9c61124d4b94050a57baff6b22b6c24fd4306ba2ec0ee7f
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
$ docker pull docker@sha256:a6ea1ff707f785adb9be2f6e47e87700acf25028f2d9967d13b76431ea6df122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74014617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0289ff325f81264fd1a632fff7b28d944ff609ba51d8209663b51d4cbd458f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
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

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6169c645a49b492d6e68d672c3d1a916c2a8e4dd3c202c56fab0c1d2be6faaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ad129589ab4978d3da3e6ef2f6e3f4f5a0ac153762f2508d8f449b0a2ca999`

```dockerfile
```

-	Layers:
	-	`sha256:8c1f247b52e1e0f2bed9ae6eabd4518ca193f0085972b55c7d23a8898a174d70`  
		Last Modified: Thu, 10 Apr 2025 18:53:49 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:14eff0079ba0251493cf5982ca5b686ca7e1593b4e2cbb96c60123f917fe8d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68957297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b7b4e4a140075fe07f7d66321e2a97fdd546d69a162a7be5bc94d5798a42dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4fb6114e207be2cba4b2c019acb8be57897e196a2e6f4dc5d987772c0b43eaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab926911105f673368ef7c6dc6b1867f1ec4adcf7e3c4945ce3c1672996fd7fd`

```dockerfile
```

-	Layers:
	-	`sha256:ed38fd2f67937dcec97c17b94519db624b47e1988d2bbbd46b9f48eac203ad8b`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:12b3a15f36a8eb6cc92894f64cb1b50a6803355bc5304a3bd83dcc90bf5ad495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67969222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e080826ce1b653f01b7fb18b04d27924f0224e0be29ad901b75a2970050ca7b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4afba38ec0f337734749f2c8b49e227a3d45f9f61389dbd68c9e7eecac222c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e89b56991dd0c0c1c8cbb2d9a7a7dc416f9f9f6b25120f4876559ffdb18d9`

```dockerfile
```

-	Layers:
	-	`sha256:279111cff860bea667d5c8682bb1a01b5bc0faf6cc7efd773554b9c7a12570c2`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:950fa733cdc541a5eaf180844e947417d625e7f1a5c2c2b11d739df98b7d0f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69756446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f62597355eb100013cdc808e76630be3420f850178b0bc0d90967c71a1c0852`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
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

### `docker:28.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:39fd6f38aadc7c0729162941c92ea691ecabb023e6d976d71ceb673074ac230c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6643e2ca409745126713435320e0adac8ab3601ef2e01b647418f12ff740aea`

```dockerfile
```

-	Layers:
	-	`sha256:0640e53e70ef0e3d76844ae18c7b1d4b97d228264c700bcd5125ddfbd7443360`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-dind`

```console
$ docker pull docker@sha256:ddb0033088b4fab74881ade341a582e3c6c8021b82377703ba1a6106bd3ded44
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
$ docker pull docker@sha256:39c7ad73456a07cc38f6201542bb8fe90af7011bbfdeedd1a38d4073f231eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141196623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915daf53f2101bf4d33fd02a660d3380b7ae93c33353b8e89d490f88d99fe063`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6fd9637e488f1aeddf77f0350669aab55ef3ba8513096467f7fdda49319b6aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c39104ed185c00634458eb4ac944cc4e3573157117d83049d13e426a8d9c82b`

```dockerfile
```

-	Layers:
	-	`sha256:d426f1591ec7aba06d77dfe270fc9e4bdf14a45b0dffdd3cc2e01d164c846f26`  
		Last Modified: Thu, 10 Apr 2025 19:01:36 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f57bfe085889a95865995e69923b8c2d367e85ce52c02e8a7104749a580824ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131831229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0574bca6d6758ad673efce2f9b025494e66ba0f910eaa2d6b6595a8e4f6358b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2be501a51d4a1f0a576d79fbe13fe078b4bdbf776ed23cf879526ede3ef5e1`  
		Last Modified: Thu, 10 Apr 2025 19:00:55 GMT  
		Size: 7.0 MB (7036868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63997f7b0bbee48aec78071d1b0c603d44f66f2ea8b8d94000c1ecaf1c6104`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 89.9 KB (89861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7912ed8760d96518614159b4b19b70b895740d64c6f5fd05d096b33364737`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd81cb731158170a092369d294fde221053b50d8bbc81edbf3e97d07bc1fbb`  
		Last Modified: Thu, 10 Apr 2025 19:00:57 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb345ef49ff2d099926b4b83939cfa58a3a46fb13ba97090b378e589e8b520`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db539f3ab5ee441f7079488bcfebcbea706e544d414404b94bdbeb9346e2dfe`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:cbd722e549eb223a43ea7d493ead3354c85f66568db49c81d21988c69328147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dff5dcf2da2754b63daf44a1ef2835e410f441cd331f7acf9f2e7e2b5b87652`

```dockerfile
```

-	Layers:
	-	`sha256:378ab517d099321cd0621b9b29b751a08fefaa9b86368894c6a55e150d700860`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:1301cf6f282edbc7d94f178d2c0eec8394d27ef4583d71f8de15d7f3dd95dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130168775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a9103d3f83801d92a29c64c17850d951bec8b8d8ff10649c9ab13809b0a5a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aad6696717cc1615cc26f88fcafdff76f694a30eb5acf705c8363975f1e651`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 6.4 MB (6366036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245fa4cf98e8dd69566bc3e134d2fac91668df09f86fdcac3355d6694aa6191c`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 86.4 KB (86355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3167df5245a23cda38488a5fe3f8e58eb4176fb82896f6995ef46c98970c9`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f510c9deee4bcd5c38974dc46e0017e99e4725922e6e4946049c7d7107a47a`  
		Last Modified: Thu, 10 Apr 2025 19:00:48 GMT  
		Size: 55.7 MB (55741207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7919e15335d560caec91132a82a0dcc2d10952d51a073120aa793accc2651f`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24e3806a3f99ba66384d8e146985e86018b9652e0c3b7d6d6773fd939fda0b`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:7265de37982ade6cf359e6c152e6c05c89d4139cd11fcb5cf319ebc88b42497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8f79d22adc370d29acb203ab10dfe28d735a51e4ba15c1b1cbaae93c747b9b`

```dockerfile
```

-	Layers:
	-	`sha256:279933e04881d0f9dd131077fec7e0243e4fb68bd92873e62fa6b7791b84d285`  
		Last Modified: Thu, 10 Apr 2025 19:00:45 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7758019ffa34f3badc161535e37606309d838fe5dc8774ff95c6f8d03371be53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132551502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6bae33c1f057ecfe982e5da8ac6862fb24634b9f314179501611fb2812e53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e6c2bff16952f87dbf0660cbc7e3b894101e54070b72fe08f5ad6760ee0fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab359cbfa98deb3b443cef392d6076cd9cae3a5f443641500ac380c6c81ffe17`

```dockerfile
```

-	Layers:
	-	`sha256:466b4a3f5e33095850c5458dc8e94c486cb9cc628b450c8e203cd9d5fb180aae`  
		Last Modified: Thu, 10 Apr 2025 19:00:50 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0-dind-rootless`

```console
$ docker pull docker@sha256:607d248e893dc10308b8f70afad4bf26cf166836856284c00c9971ec9d9e7dc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0-dind-rootless` - linux; amd64

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

### `docker:28.0-dind-rootless` - unknown; unknown

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

### `docker:28.0-dind-rootless` - linux; arm64 variant v8

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

### `docker:28.0-dind-rootless` - unknown; unknown

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

## `docker:28.0-windowsservercore`

```console
$ docker pull docker@sha256:b4976a3b828001015b15b82f7164b772b541d63c40ff57d25001d0a654e09e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `docker:28.0-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8084d47f9c866ffb0fc6c74d818412ff1196f96066e4460f40ddb325112e0dcc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3460019679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8eb0a28181dcd66cffe910466b7bc06081957269945180b9e3be0f83af31bd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:39:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:39:26 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:39:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:39:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:39:39 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:39:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:39:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:39:50 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:39:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90663cbdd92914b16d1b360ec39197f6848f810c2e3d5f75368367b755fb29a5`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6859709f79778e74c7ef624e307d1930c0f780d10be536cb85d9893936b1d2`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 364.7 KB (364741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f3f9fb8993e6eddeb12b79a24923159ad4bba9c61def71fa12ee3f22eb949b`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b566c3c24e01288e140412f9834c019e4e2e71145ed6b6b079795f86b97424f2`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc5f946c4df03788d89b893a24b781d0bf21407cc2582ef5194f0eaea08db74`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 19.9 MB (19876882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2a3d26ad4275972b61ccdede64c0ddf0788bfa910b1275b74d172e5082198`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ad96060e962414395bc1991729228e8ca1e139d5b228efc120a55e2b9cab5`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb45857c62165be6ffbdcee3d0a6ae915dec7440305fc6ebfc274ca67879d0de`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946bf5bea56a89ae65bdacd4edde0517f360ff8ebcabd76df02411213a273c01`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.8 MB (22779634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6100d6c301fb149b342ede708f60d3cb8e10a3c1e9e3836c1baf34221724cef0`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d08118b8b7f3b7ff9643a05fa0fabf35417f346904745264b1b7878d575e1d`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8922e187bf58aaae3a9c3e2e9e8cfb6b00b0ad16a4e8cd5a47b91da0443a6`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93978eb25ad6c40ce8eccddc334dfe92007d5cc7ed7df32eaef8dd97ec678442`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.3 MB (22307251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:0fe4c4d0f5c80021c50c85d104ea9454679f65eef396c515473415b2f3551677
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336245643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2260686200048a8ce26b4461ef2e6b0b73d9ce4353bad23921ebc2a3c91998b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:53:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:53:44 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:53:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:53:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:53:56 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:54:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:54:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:54:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd31ce4b72c969f090b09e0d47519bd245635b8a0766cad50a94e5285269e7f`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611d42417bb7b25c9cbe870a1d686b89d1d9756d80d42e4fd6e078d9f81ce4a`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 346.1 KB (346062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb06dc8ecf1b08f1190ad1c0d83e1fdabc1c8d67fc1ac6cb12116132b4f03468`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008480b629bc35e084765059b6f319dc7ff56f6ddd835cde71f710a1d1b3d636`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c50ac98d04810f7b347835e962e1cc758aeb4ba0ee8a7231139b95c1d2bde`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 19.9 MB (19852659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107085d17762a97b5dc8bd94314f73c5a529607173545e1afaca9a1d379c104d`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271fac6913f53452e4c148e110e15c1cf204cafbed62e7609172534dea68b05f`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c075328080e6995af18ba0d46caacfb2d481e3bfd03bd1e1feb30c92ef355`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff40e518cab6103cc2dbbed344e68095afb68f480c2690b74900f7a7412e1ae9`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 22.8 MB (22756339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a62709feb8f58e8269a332f8cb621fcd984c1c3316283ccded16919bf71cda`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6acbdb8f48fcce734907c9a41f60cd59f358e65c812a3a4981f5e8b3276d52e`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1edc9932a94ae1c328f7a4190d5780f481b8890967cbc0e915a092e9a8f0871`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececc62a636024315de22ccaac302436c36e77452a38b7f08b83dca6b0795455`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 22.3 MB (22283301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:fa94327469822a56e83053ec60f804486fe9ee64c9f15be87233d2651926c32b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227933081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffec676bac1f14cd20f776a437da6b9fe135a587eb81263ff81adc16bb644ca6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 01:19:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:19:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 01:19:53 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 01:19:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 01:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 01:20:09 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 01:20:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 01:20:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 01:20:20 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 01:20:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243c89dd211d21587050138b4ba9caca0157449d59d6698f399bda8c9ac09647`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a64f1cb97b9459857deaad35fc7cb3146d6d807da8b42954f5570e8015ff8d`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 331.8 KB (331794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1ff6cf58cfc4c73c2c1cb14b2dbd5e91ccd8342cf3e7b4979f8c273605063b`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e961a01ad0f71ba1051d35d21755803b2fa1951fba5c545b345c4ddb497d4cf`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba307589781f303a1e20fe2f5c8a65fe379191b2f06f8de840ea2aaecf184f47`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 19.8 MB (19844611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb7ebad4ed4801f9cb8c8b750ab2454c93c826a400f3e5ac972a921b43dd3f2`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55c409429d09b5ed5634e52d87d957962d25ed1cd4d0dd5b62783cd4e2f446`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd36acd6048ee7eb5e37f47ea0ed75fb4bbcc90983346c92ae7cc8a3a43aa0a`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4383de892731480789dbba3ea542e0493a181b4619b7feb20fdd1701337750`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.7 MB (22748533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7686b51d722ad3222e89104c832b025336bd4a4a7c2beb26fa7eb95875deafbd`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cb46454301b3cc3fcacd9a425240920b39672c040ac885da807dfc3a33746f`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e72a7a6e8ddcef11a9b230a1cec67389895ec62572710f439e53ed43a59c019`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88569070dd26d817476810a2cd6ad26ea8f4e775ccdf912cbf72eef0203286a`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.3 MB (22270587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:cc2efcf0a0bafa3c9df47a975aa3a6f095645104779c3b74fa0ff3ec9b2e1e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `docker:28.0-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:fa94327469822a56e83053ec60f804486fe9ee64c9f15be87233d2651926c32b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227933081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffec676bac1f14cd20f776a437da6b9fe135a587eb81263ff81adc16bb644ca6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 01:19:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:19:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 01:19:53 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 01:19:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 01:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 01:20:09 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 01:20:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 01:20:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 01:20:20 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 01:20:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243c89dd211d21587050138b4ba9caca0157449d59d6698f399bda8c9ac09647`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a64f1cb97b9459857deaad35fc7cb3146d6d807da8b42954f5570e8015ff8d`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 331.8 KB (331794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1ff6cf58cfc4c73c2c1cb14b2dbd5e91ccd8342cf3e7b4979f8c273605063b`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e961a01ad0f71ba1051d35d21755803b2fa1951fba5c545b345c4ddb497d4cf`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba307589781f303a1e20fe2f5c8a65fe379191b2f06f8de840ea2aaecf184f47`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 19.8 MB (19844611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb7ebad4ed4801f9cb8c8b750ab2454c93c826a400f3e5ac972a921b43dd3f2`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55c409429d09b5ed5634e52d87d957962d25ed1cd4d0dd5b62783cd4e2f446`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd36acd6048ee7eb5e37f47ea0ed75fb4bbcc90983346c92ae7cc8a3a43aa0a`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4383de892731480789dbba3ea542e0493a181b4619b7feb20fdd1701337750`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.7 MB (22748533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7686b51d722ad3222e89104c832b025336bd4a4a7c2beb26fa7eb95875deafbd`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cb46454301b3cc3fcacd9a425240920b39672c040ac885da807dfc3a33746f`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e72a7a6e8ddcef11a9b230a1cec67389895ec62572710f439e53ed43a59c019`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88569070dd26d817476810a2cd6ad26ea8f4e775ccdf912cbf72eef0203286a`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.3 MB (22270587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fe87151fca5614738a9a2377a76c82a06dcd81fa4827ccffb171958d6fb8494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `docker:28.0-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:0fe4c4d0f5c80021c50c85d104ea9454679f65eef396c515473415b2f3551677
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336245643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2260686200048a8ce26b4461ef2e6b0b73d9ce4353bad23921ebc2a3c91998b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:53:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:53:44 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:53:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:53:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:53:56 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:54:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:54:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:54:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd31ce4b72c969f090b09e0d47519bd245635b8a0766cad50a94e5285269e7f`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611d42417bb7b25c9cbe870a1d686b89d1d9756d80d42e4fd6e078d9f81ce4a`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 346.1 KB (346062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb06dc8ecf1b08f1190ad1c0d83e1fdabc1c8d67fc1ac6cb12116132b4f03468`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008480b629bc35e084765059b6f319dc7ff56f6ddd835cde71f710a1d1b3d636`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c50ac98d04810f7b347835e962e1cc758aeb4ba0ee8a7231139b95c1d2bde`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 19.9 MB (19852659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107085d17762a97b5dc8bd94314f73c5a529607173545e1afaca9a1d379c104d`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271fac6913f53452e4c148e110e15c1cf204cafbed62e7609172534dea68b05f`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c075328080e6995af18ba0d46caacfb2d481e3bfd03bd1e1feb30c92ef355`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff40e518cab6103cc2dbbed344e68095afb68f480c2690b74900f7a7412e1ae9`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 22.8 MB (22756339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a62709feb8f58e8269a332f8cb621fcd984c1c3316283ccded16919bf71cda`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6acbdb8f48fcce734907c9a41f60cd59f358e65c812a3a4981f5e8b3276d52e`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1edc9932a94ae1c328f7a4190d5780f481b8890967cbc0e915a092e9a8f0871`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececc62a636024315de22ccaac302436c36e77452a38b7f08b83dca6b0795455`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 22.3 MB (22283301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:7aacee74867dda438d28dbabea6db4a5d0891bc6ef5f0174dcd201910d0b3d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `docker:28.0-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8084d47f9c866ffb0fc6c74d818412ff1196f96066e4460f40ddb325112e0dcc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3460019679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8eb0a28181dcd66cffe910466b7bc06081957269945180b9e3be0f83af31bd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:39:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:39:26 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:39:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:39:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:39:39 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:39:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:39:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:39:50 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:39:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90663cbdd92914b16d1b360ec39197f6848f810c2e3d5f75368367b755fb29a5`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6859709f79778e74c7ef624e307d1930c0f780d10be536cb85d9893936b1d2`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 364.7 KB (364741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f3f9fb8993e6eddeb12b79a24923159ad4bba9c61def71fa12ee3f22eb949b`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b566c3c24e01288e140412f9834c019e4e2e71145ed6b6b079795f86b97424f2`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc5f946c4df03788d89b893a24b781d0bf21407cc2582ef5194f0eaea08db74`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 19.9 MB (19876882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2a3d26ad4275972b61ccdede64c0ddf0788bfa910b1275b74d172e5082198`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ad96060e962414395bc1991729228e8ca1e139d5b228efc120a55e2b9cab5`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb45857c62165be6ffbdcee3d0a6ae915dec7440305fc6ebfc274ca67879d0de`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946bf5bea56a89ae65bdacd4edde0517f360ff8ebcabd76df02411213a273c01`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.8 MB (22779634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6100d6c301fb149b342ede708f60d3cb8e10a3c1e9e3836c1baf34221724cef0`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d08118b8b7f3b7ff9643a05fa0fabf35417f346904745264b1b7878d575e1d`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8922e187bf58aaae3a9c3e2e9e8cfb6b00b0ad16a4e8cd5a47b91da0443a6`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93978eb25ad6c40ce8eccddc334dfe92007d5cc7ed7df32eaef8dd97ec678442`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.3 MB (22307251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.4`

```console
$ docker pull docker@sha256:ddb0033088b4fab74881ade341a582e3c6c8021b82377703ba1a6106bd3ded44
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

### `docker:28.0.4` - linux; amd64

```console
$ docker pull docker@sha256:39c7ad73456a07cc38f6201542bb8fe90af7011bbfdeedd1a38d4073f231eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141196623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915daf53f2101bf4d33fd02a660d3380b7ae93c33353b8e89d490f88d99fe063`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0.4` - unknown; unknown

```console
$ docker pull docker@sha256:6fd9637e488f1aeddf77f0350669aab55ef3ba8513096467f7fdda49319b6aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c39104ed185c00634458eb4ac944cc4e3573157117d83049d13e426a8d9c82b`

```dockerfile
```

-	Layers:
	-	`sha256:d426f1591ec7aba06d77dfe270fc9e4bdf14a45b0dffdd3cc2e01d164c846f26`  
		Last Modified: Thu, 10 Apr 2025 19:01:36 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4` - linux; arm variant v6

```console
$ docker pull docker@sha256:f57bfe085889a95865995e69923b8c2d367e85ce52c02e8a7104749a580824ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131831229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0574bca6d6758ad673efce2f9b025494e66ba0f910eaa2d6b6595a8e4f6358b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2be501a51d4a1f0a576d79fbe13fe078b4bdbf776ed23cf879526ede3ef5e1`  
		Last Modified: Thu, 10 Apr 2025 19:00:55 GMT  
		Size: 7.0 MB (7036868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63997f7b0bbee48aec78071d1b0c603d44f66f2ea8b8d94000c1ecaf1c6104`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 89.9 KB (89861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7912ed8760d96518614159b4b19b70b895740d64c6f5fd05d096b33364737`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd81cb731158170a092369d294fde221053b50d8bbc81edbf3e97d07bc1fbb`  
		Last Modified: Thu, 10 Apr 2025 19:00:57 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb345ef49ff2d099926b4b83939cfa58a3a46fb13ba97090b378e589e8b520`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db539f3ab5ee441f7079488bcfebcbea706e544d414404b94bdbeb9346e2dfe`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4` - unknown; unknown

```console
$ docker pull docker@sha256:cbd722e549eb223a43ea7d493ead3354c85f66568db49c81d21988c69328147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dff5dcf2da2754b63daf44a1ef2835e410f441cd331f7acf9f2e7e2b5b87652`

```dockerfile
```

-	Layers:
	-	`sha256:378ab517d099321cd0621b9b29b751a08fefaa9b86368894c6a55e150d700860`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4` - linux; arm variant v7

```console
$ docker pull docker@sha256:1301cf6f282edbc7d94f178d2c0eec8394d27ef4583d71f8de15d7f3dd95dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130168775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a9103d3f83801d92a29c64c17850d951bec8b8d8ff10649c9ab13809b0a5a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aad6696717cc1615cc26f88fcafdff76f694a30eb5acf705c8363975f1e651`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 6.4 MB (6366036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245fa4cf98e8dd69566bc3e134d2fac91668df09f86fdcac3355d6694aa6191c`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 86.4 KB (86355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3167df5245a23cda38488a5fe3f8e58eb4176fb82896f6995ef46c98970c9`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f510c9deee4bcd5c38974dc46e0017e99e4725922e6e4946049c7d7107a47a`  
		Last Modified: Thu, 10 Apr 2025 19:00:48 GMT  
		Size: 55.7 MB (55741207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7919e15335d560caec91132a82a0dcc2d10952d51a073120aa793accc2651f`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24e3806a3f99ba66384d8e146985e86018b9652e0c3b7d6d6773fd939fda0b`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4` - unknown; unknown

```console
$ docker pull docker@sha256:7265de37982ade6cf359e6c152e6c05c89d4139cd11fcb5cf319ebc88b42497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8f79d22adc370d29acb203ab10dfe28d735a51e4ba15c1b1cbaae93c747b9b`

```dockerfile
```

-	Layers:
	-	`sha256:279933e04881d0f9dd131077fec7e0243e4fb68bd92873e62fa6b7791b84d285`  
		Last Modified: Thu, 10 Apr 2025 19:00:45 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7758019ffa34f3badc161535e37606309d838fe5dc8774ff95c6f8d03371be53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132551502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6bae33c1f057ecfe982e5da8ac6862fb24634b9f314179501611fb2812e53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0.4` - unknown; unknown

```console
$ docker pull docker@sha256:e6c2bff16952f87dbf0660cbc7e3b894101e54070b72fe08f5ad6760ee0fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab359cbfa98deb3b443cef392d6076cd9cae3a5f443641500ac380c6c81ffe17`

```dockerfile
```

-	Layers:
	-	`sha256:466b4a3f5e33095850c5458dc8e94c486cb9cc628b450c8e203cd9d5fb180aae`  
		Last Modified: Thu, 10 Apr 2025 19:00:50 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-alpine3.21`

```console
$ docker pull docker@sha256:ddb0033088b4fab74881ade341a582e3c6c8021b82377703ba1a6106bd3ded44
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

### `docker:28.0.4-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:39c7ad73456a07cc38f6201542bb8fe90af7011bbfdeedd1a38d4073f231eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141196623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915daf53f2101bf4d33fd02a660d3380b7ae93c33353b8e89d490f88d99fe063`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0.4-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:6fd9637e488f1aeddf77f0350669aab55ef3ba8513096467f7fdda49319b6aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c39104ed185c00634458eb4ac944cc4e3573157117d83049d13e426a8d9c82b`

```dockerfile
```

-	Layers:
	-	`sha256:d426f1591ec7aba06d77dfe270fc9e4bdf14a45b0dffdd3cc2e01d164c846f26`  
		Last Modified: Thu, 10 Apr 2025 19:01:36 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:f57bfe085889a95865995e69923b8c2d367e85ce52c02e8a7104749a580824ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131831229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0574bca6d6758ad673efce2f9b025494e66ba0f910eaa2d6b6595a8e4f6358b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2be501a51d4a1f0a576d79fbe13fe078b4bdbf776ed23cf879526ede3ef5e1`  
		Last Modified: Thu, 10 Apr 2025 19:00:55 GMT  
		Size: 7.0 MB (7036868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63997f7b0bbee48aec78071d1b0c603d44f66f2ea8b8d94000c1ecaf1c6104`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 89.9 KB (89861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7912ed8760d96518614159b4b19b70b895740d64c6f5fd05d096b33364737`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd81cb731158170a092369d294fde221053b50d8bbc81edbf3e97d07bc1fbb`  
		Last Modified: Thu, 10 Apr 2025 19:00:57 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb345ef49ff2d099926b4b83939cfa58a3a46fb13ba97090b378e589e8b520`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db539f3ab5ee441f7079488bcfebcbea706e544d414404b94bdbeb9346e2dfe`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:cbd722e549eb223a43ea7d493ead3354c85f66568db49c81d21988c69328147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dff5dcf2da2754b63daf44a1ef2835e410f441cd331f7acf9f2e7e2b5b87652`

```dockerfile
```

-	Layers:
	-	`sha256:378ab517d099321cd0621b9b29b751a08fefaa9b86368894c6a55e150d700860`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:1301cf6f282edbc7d94f178d2c0eec8394d27ef4583d71f8de15d7f3dd95dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130168775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a9103d3f83801d92a29c64c17850d951bec8b8d8ff10649c9ab13809b0a5a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aad6696717cc1615cc26f88fcafdff76f694a30eb5acf705c8363975f1e651`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 6.4 MB (6366036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245fa4cf98e8dd69566bc3e134d2fac91668df09f86fdcac3355d6694aa6191c`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 86.4 KB (86355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3167df5245a23cda38488a5fe3f8e58eb4176fb82896f6995ef46c98970c9`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f510c9deee4bcd5c38974dc46e0017e99e4725922e6e4946049c7d7107a47a`  
		Last Modified: Thu, 10 Apr 2025 19:00:48 GMT  
		Size: 55.7 MB (55741207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7919e15335d560caec91132a82a0dcc2d10952d51a073120aa793accc2651f`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24e3806a3f99ba66384d8e146985e86018b9652e0c3b7d6d6773fd939fda0b`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:7265de37982ade6cf359e6c152e6c05c89d4139cd11fcb5cf319ebc88b42497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8f79d22adc370d29acb203ab10dfe28d735a51e4ba15c1b1cbaae93c747b9b`

```dockerfile
```

-	Layers:
	-	`sha256:279933e04881d0f9dd131077fec7e0243e4fb68bd92873e62fa6b7791b84d285`  
		Last Modified: Thu, 10 Apr 2025 19:00:45 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7758019ffa34f3badc161535e37606309d838fe5dc8774ff95c6f8d03371be53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132551502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6bae33c1f057ecfe982e5da8ac6862fb24634b9f314179501611fb2812e53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0.4-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:e6c2bff16952f87dbf0660cbc7e3b894101e54070b72fe08f5ad6760ee0fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab359cbfa98deb3b443cef392d6076cd9cae3a5f443641500ac380c6c81ffe17`

```dockerfile
```

-	Layers:
	-	`sha256:466b4a3f5e33095850c5458dc8e94c486cb9cc628b450c8e203cd9d5fb180aae`  
		Last Modified: Thu, 10 Apr 2025 19:00:50 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-cli`

```console
$ docker pull docker@sha256:db3ecdf8e404584aa9c61124d4b94050a57baff6b22b6c24fd4306ba2ec0ee7f
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

### `docker:28.0.4-cli` - linux; amd64

```console
$ docker pull docker@sha256:a6ea1ff707f785adb9be2f6e47e87700acf25028f2d9967d13b76431ea6df122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74014617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0289ff325f81264fd1a632fff7b28d944ff609ba51d8209663b51d4cbd458f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
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

### `docker:28.0.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6169c645a49b492d6e68d672c3d1a916c2a8e4dd3c202c56fab0c1d2be6faaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ad129589ab4978d3da3e6ef2f6e3f4f5a0ac153762f2508d8f449b0a2ca999`

```dockerfile
```

-	Layers:
	-	`sha256:8c1f247b52e1e0f2bed9ae6eabd4518ca193f0085972b55c7d23a8898a174d70`  
		Last Modified: Thu, 10 Apr 2025 18:53:49 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:14eff0079ba0251493cf5982ca5b686ca7e1593b4e2cbb96c60123f917fe8d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68957297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b7b4e4a140075fe07f7d66321e2a97fdd546d69a162a7be5bc94d5798a42dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4fb6114e207be2cba4b2c019acb8be57897e196a2e6f4dc5d987772c0b43eaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab926911105f673368ef7c6dc6b1867f1ec4adcf7e3c4945ce3c1672996fd7fd`

```dockerfile
```

-	Layers:
	-	`sha256:ed38fd2f67937dcec97c17b94519db624b47e1988d2bbbd46b9f48eac203ad8b`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:12b3a15f36a8eb6cc92894f64cb1b50a6803355bc5304a3bd83dcc90bf5ad495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67969222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e080826ce1b653f01b7fb18b04d27924f0224e0be29ad901b75a2970050ca7b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:4afba38ec0f337734749f2c8b49e227a3d45f9f61389dbd68c9e7eecac222c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e89b56991dd0c0c1c8cbb2d9a7a7dc416f9f9f6b25120f4876559ffdb18d9`

```dockerfile
```

-	Layers:
	-	`sha256:279111cff860bea667d5c8682bb1a01b5bc0faf6cc7efd773554b9c7a12570c2`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:950fa733cdc541a5eaf180844e947417d625e7f1a5c2c2b11d739df98b7d0f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69756446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f62597355eb100013cdc808e76630be3420f850178b0bc0d90967c71a1c0852`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
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

### `docker:28.0.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:39fd6f38aadc7c0729162941c92ea691ecabb023e6d976d71ceb673074ac230c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6643e2ca409745126713435320e0adac8ab3601ef2e01b647418f12ff740aea`

```dockerfile
```

-	Layers:
	-	`sha256:0640e53e70ef0e3d76844ae18c7b1d4b97d228264c700bcd5125ddfbd7443360`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-cli-alpine3.21`

```console
$ docker pull docker@sha256:db3ecdf8e404584aa9c61124d4b94050a57baff6b22b6c24fd4306ba2ec0ee7f
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

### `docker:28.0.4-cli-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:a6ea1ff707f785adb9be2f6e47e87700acf25028f2d9967d13b76431ea6df122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74014617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0289ff325f81264fd1a632fff7b28d944ff609ba51d8209663b51d4cbd458f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
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

### `docker:28.0.4-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:a6169c645a49b492d6e68d672c3d1a916c2a8e4dd3c202c56fab0c1d2be6faaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ad129589ab4978d3da3e6ef2f6e3f4f5a0ac153762f2508d8f449b0a2ca999`

```dockerfile
```

-	Layers:
	-	`sha256:8c1f247b52e1e0f2bed9ae6eabd4518ca193f0085972b55c7d23a8898a174d70`  
		Last Modified: Thu, 10 Apr 2025 18:53:49 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:14eff0079ba0251493cf5982ca5b686ca7e1593b4e2cbb96c60123f917fe8d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68957297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b7b4e4a140075fe07f7d66321e2a97fdd546d69a162a7be5bc94d5798a42dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4fb6114e207be2cba4b2c019acb8be57897e196a2e6f4dc5d987772c0b43eaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab926911105f673368ef7c6dc6b1867f1ec4adcf7e3c4945ce3c1672996fd7fd`

```dockerfile
```

-	Layers:
	-	`sha256:ed38fd2f67937dcec97c17b94519db624b47e1988d2bbbd46b9f48eac203ad8b`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:12b3a15f36a8eb6cc92894f64cb1b50a6803355bc5304a3bd83dcc90bf5ad495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67969222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e080826ce1b653f01b7fb18b04d27924f0224e0be29ad901b75a2970050ca7b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:4afba38ec0f337734749f2c8b49e227a3d45f9f61389dbd68c9e7eecac222c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e89b56991dd0c0c1c8cbb2d9a7a7dc416f9f9f6b25120f4876559ffdb18d9`

```dockerfile
```

-	Layers:
	-	`sha256:279111cff860bea667d5c8682bb1a01b5bc0faf6cc7efd773554b9c7a12570c2`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-cli-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:950fa733cdc541a5eaf180844e947417d625e7f1a5c2c2b11d739df98b7d0f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69756446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f62597355eb100013cdc808e76630be3420f850178b0bc0d90967c71a1c0852`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
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

### `docker:28.0.4-cli-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:39fd6f38aadc7c0729162941c92ea691ecabb023e6d976d71ceb673074ac230c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6643e2ca409745126713435320e0adac8ab3601ef2e01b647418f12ff740aea`

```dockerfile
```

-	Layers:
	-	`sha256:0640e53e70ef0e3d76844ae18c7b1d4b97d228264c700bcd5125ddfbd7443360`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-dind`

```console
$ docker pull docker@sha256:ddb0033088b4fab74881ade341a582e3c6c8021b82377703ba1a6106bd3ded44
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

### `docker:28.0.4-dind` - linux; amd64

```console
$ docker pull docker@sha256:39c7ad73456a07cc38f6201542bb8fe90af7011bbfdeedd1a38d4073f231eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141196623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915daf53f2101bf4d33fd02a660d3380b7ae93c33353b8e89d490f88d99fe063`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6fd9637e488f1aeddf77f0350669aab55ef3ba8513096467f7fdda49319b6aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c39104ed185c00634458eb4ac944cc4e3573157117d83049d13e426a8d9c82b`

```dockerfile
```

-	Layers:
	-	`sha256:d426f1591ec7aba06d77dfe270fc9e4bdf14a45b0dffdd3cc2e01d164c846f26`  
		Last Modified: Thu, 10 Apr 2025 19:01:36 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f57bfe085889a95865995e69923b8c2d367e85ce52c02e8a7104749a580824ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131831229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0574bca6d6758ad673efce2f9b025494e66ba0f910eaa2d6b6595a8e4f6358b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2be501a51d4a1f0a576d79fbe13fe078b4bdbf776ed23cf879526ede3ef5e1`  
		Last Modified: Thu, 10 Apr 2025 19:00:55 GMT  
		Size: 7.0 MB (7036868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63997f7b0bbee48aec78071d1b0c603d44f66f2ea8b8d94000c1ecaf1c6104`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 89.9 KB (89861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7912ed8760d96518614159b4b19b70b895740d64c6f5fd05d096b33364737`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd81cb731158170a092369d294fde221053b50d8bbc81edbf3e97d07bc1fbb`  
		Last Modified: Thu, 10 Apr 2025 19:00:57 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb345ef49ff2d099926b4b83939cfa58a3a46fb13ba97090b378e589e8b520`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db539f3ab5ee441f7079488bcfebcbea706e544d414404b94bdbeb9346e2dfe`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:cbd722e549eb223a43ea7d493ead3354c85f66568db49c81d21988c69328147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dff5dcf2da2754b63daf44a1ef2835e410f441cd331f7acf9f2e7e2b5b87652`

```dockerfile
```

-	Layers:
	-	`sha256:378ab517d099321cd0621b9b29b751a08fefaa9b86368894c6a55e150d700860`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:1301cf6f282edbc7d94f178d2c0eec8394d27ef4583d71f8de15d7f3dd95dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130168775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a9103d3f83801d92a29c64c17850d951bec8b8d8ff10649c9ab13809b0a5a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aad6696717cc1615cc26f88fcafdff76f694a30eb5acf705c8363975f1e651`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 6.4 MB (6366036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245fa4cf98e8dd69566bc3e134d2fac91668df09f86fdcac3355d6694aa6191c`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 86.4 KB (86355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3167df5245a23cda38488a5fe3f8e58eb4176fb82896f6995ef46c98970c9`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f510c9deee4bcd5c38974dc46e0017e99e4725922e6e4946049c7d7107a47a`  
		Last Modified: Thu, 10 Apr 2025 19:00:48 GMT  
		Size: 55.7 MB (55741207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7919e15335d560caec91132a82a0dcc2d10952d51a073120aa793accc2651f`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24e3806a3f99ba66384d8e146985e86018b9652e0c3b7d6d6773fd939fda0b`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:7265de37982ade6cf359e6c152e6c05c89d4139cd11fcb5cf319ebc88b42497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8f79d22adc370d29acb203ab10dfe28d735a51e4ba15c1b1cbaae93c747b9b`

```dockerfile
```

-	Layers:
	-	`sha256:279933e04881d0f9dd131077fec7e0243e4fb68bd92873e62fa6b7791b84d285`  
		Last Modified: Thu, 10 Apr 2025 19:00:45 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7758019ffa34f3badc161535e37606309d838fe5dc8774ff95c6f8d03371be53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132551502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6bae33c1f057ecfe982e5da8ac6862fb24634b9f314179501611fb2812e53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:e6c2bff16952f87dbf0660cbc7e3b894101e54070b72fe08f5ad6760ee0fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab359cbfa98deb3b443cef392d6076cd9cae3a5f443641500ac380c6c81ffe17`

```dockerfile
```

-	Layers:
	-	`sha256:466b4a3f5e33095850c5458dc8e94c486cb9cc628b450c8e203cd9d5fb180aae`  
		Last Modified: Thu, 10 Apr 2025 19:00:50 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-dind-alpine3.21`

```console
$ docker pull docker@sha256:ddb0033088b4fab74881ade341a582e3c6c8021b82377703ba1a6106bd3ded44
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

### `docker:28.0.4-dind-alpine3.21` - linux; amd64

```console
$ docker pull docker@sha256:39c7ad73456a07cc38f6201542bb8fe90af7011bbfdeedd1a38d4073f231eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141196623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915daf53f2101bf4d33fd02a660d3380b7ae93c33353b8e89d490f88d99fe063`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0.4-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:6fd9637e488f1aeddf77f0350669aab55ef3ba8513096467f7fdda49319b6aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c39104ed185c00634458eb4ac944cc4e3573157117d83049d13e426a8d9c82b`

```dockerfile
```

-	Layers:
	-	`sha256:d426f1591ec7aba06d77dfe270fc9e4bdf14a45b0dffdd3cc2e01d164c846f26`  
		Last Modified: Thu, 10 Apr 2025 19:01:36 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind-alpine3.21` - linux; arm variant v6

```console
$ docker pull docker@sha256:f57bfe085889a95865995e69923b8c2d367e85ce52c02e8a7104749a580824ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131831229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0574bca6d6758ad673efce2f9b025494e66ba0f910eaa2d6b6595a8e4f6358b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2be501a51d4a1f0a576d79fbe13fe078b4bdbf776ed23cf879526ede3ef5e1`  
		Last Modified: Thu, 10 Apr 2025 19:00:55 GMT  
		Size: 7.0 MB (7036868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63997f7b0bbee48aec78071d1b0c603d44f66f2ea8b8d94000c1ecaf1c6104`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 89.9 KB (89861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7912ed8760d96518614159b4b19b70b895740d64c6f5fd05d096b33364737`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd81cb731158170a092369d294fde221053b50d8bbc81edbf3e97d07bc1fbb`  
		Last Modified: Thu, 10 Apr 2025 19:00:57 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb345ef49ff2d099926b4b83939cfa58a3a46fb13ba97090b378e589e8b520`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db539f3ab5ee441f7079488bcfebcbea706e544d414404b94bdbeb9346e2dfe`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:cbd722e549eb223a43ea7d493ead3354c85f66568db49c81d21988c69328147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dff5dcf2da2754b63daf44a1ef2835e410f441cd331f7acf9f2e7e2b5b87652`

```dockerfile
```

-	Layers:
	-	`sha256:378ab517d099321cd0621b9b29b751a08fefaa9b86368894c6a55e150d700860`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind-alpine3.21` - linux; arm variant v7

```console
$ docker pull docker@sha256:1301cf6f282edbc7d94f178d2c0eec8394d27ef4583d71f8de15d7f3dd95dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130168775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a9103d3f83801d92a29c64c17850d951bec8b8d8ff10649c9ab13809b0a5a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aad6696717cc1615cc26f88fcafdff76f694a30eb5acf705c8363975f1e651`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 6.4 MB (6366036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245fa4cf98e8dd69566bc3e134d2fac91668df09f86fdcac3355d6694aa6191c`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 86.4 KB (86355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3167df5245a23cda38488a5fe3f8e58eb4176fb82896f6995ef46c98970c9`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f510c9deee4bcd5c38974dc46e0017e99e4725922e6e4946049c7d7107a47a`  
		Last Modified: Thu, 10 Apr 2025 19:00:48 GMT  
		Size: 55.7 MB (55741207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7919e15335d560caec91132a82a0dcc2d10952d51a073120aa793accc2651f`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24e3806a3f99ba66384d8e146985e86018b9652e0c3b7d6d6773fd939fda0b`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.0.4-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:7265de37982ade6cf359e6c152e6c05c89d4139cd11fcb5cf319ebc88b42497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8f79d22adc370d29acb203ab10dfe28d735a51e4ba15c1b1cbaae93c747b9b`

```dockerfile
```

-	Layers:
	-	`sha256:279933e04881d0f9dd131077fec7e0243e4fb68bd92873e62fa6b7791b84d285`  
		Last Modified: Thu, 10 Apr 2025 19:00:45 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.0.4-dind-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7758019ffa34f3badc161535e37606309d838fe5dc8774ff95c6f8d03371be53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132551502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6bae33c1f057ecfe982e5da8ac6862fb24634b9f314179501611fb2812e53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:28.0.4-dind-alpine3.21` - unknown; unknown

```console
$ docker pull docker@sha256:e6c2bff16952f87dbf0660cbc7e3b894101e54070b72fe08f5ad6760ee0fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab359cbfa98deb3b443cef392d6076cd9cae3a5f443641500ac380c6c81ffe17`

```dockerfile
```

-	Layers:
	-	`sha256:466b4a3f5e33095850c5458dc8e94c486cb9cc628b450c8e203cd9d5fb180aae`  
		Last Modified: Thu, 10 Apr 2025 19:00:50 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.0.4-dind-rootless`

```console
$ docker pull docker@sha256:607d248e893dc10308b8f70afad4bf26cf166836856284c00c9971ec9d9e7dc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.0.4-dind-rootless` - linux; amd64

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

### `docker:28.0.4-dind-rootless` - unknown; unknown

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

### `docker:28.0.4-dind-rootless` - linux; arm64 variant v8

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

### `docker:28.0.4-dind-rootless` - unknown; unknown

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

## `docker:28.0.4-windowsservercore`

```console
$ docker pull docker@sha256:b4976a3b828001015b15b82f7164b772b541d63c40ff57d25001d0a654e09e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `docker:28.0.4-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8084d47f9c866ffb0fc6c74d818412ff1196f96066e4460f40ddb325112e0dcc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3460019679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8eb0a28181dcd66cffe910466b7bc06081957269945180b9e3be0f83af31bd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:39:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:39:26 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:39:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:39:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:39:39 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:39:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:39:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:39:50 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:39:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90663cbdd92914b16d1b360ec39197f6848f810c2e3d5f75368367b755fb29a5`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6859709f79778e74c7ef624e307d1930c0f780d10be536cb85d9893936b1d2`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 364.7 KB (364741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f3f9fb8993e6eddeb12b79a24923159ad4bba9c61def71fa12ee3f22eb949b`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b566c3c24e01288e140412f9834c019e4e2e71145ed6b6b079795f86b97424f2`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc5f946c4df03788d89b893a24b781d0bf21407cc2582ef5194f0eaea08db74`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 19.9 MB (19876882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2a3d26ad4275972b61ccdede64c0ddf0788bfa910b1275b74d172e5082198`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ad96060e962414395bc1991729228e8ca1e139d5b228efc120a55e2b9cab5`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb45857c62165be6ffbdcee3d0a6ae915dec7440305fc6ebfc274ca67879d0de`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946bf5bea56a89ae65bdacd4edde0517f360ff8ebcabd76df02411213a273c01`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.8 MB (22779634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6100d6c301fb149b342ede708f60d3cb8e10a3c1e9e3836c1baf34221724cef0`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d08118b8b7f3b7ff9643a05fa0fabf35417f346904745264b1b7878d575e1d`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8922e187bf58aaae3a9c3e2e9e8cfb6b00b0ad16a4e8cd5a47b91da0443a6`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93978eb25ad6c40ce8eccddc334dfe92007d5cc7ed7df32eaef8dd97ec678442`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.3 MB (22307251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.4-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:0fe4c4d0f5c80021c50c85d104ea9454679f65eef396c515473415b2f3551677
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336245643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2260686200048a8ce26b4461ef2e6b0b73d9ce4353bad23921ebc2a3c91998b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:53:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:53:44 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:53:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:53:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:53:56 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:54:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:54:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:54:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd31ce4b72c969f090b09e0d47519bd245635b8a0766cad50a94e5285269e7f`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611d42417bb7b25c9cbe870a1d686b89d1d9756d80d42e4fd6e078d9f81ce4a`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 346.1 KB (346062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb06dc8ecf1b08f1190ad1c0d83e1fdabc1c8d67fc1ac6cb12116132b4f03468`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008480b629bc35e084765059b6f319dc7ff56f6ddd835cde71f710a1d1b3d636`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c50ac98d04810f7b347835e962e1cc758aeb4ba0ee8a7231139b95c1d2bde`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 19.9 MB (19852659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107085d17762a97b5dc8bd94314f73c5a529607173545e1afaca9a1d379c104d`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271fac6913f53452e4c148e110e15c1cf204cafbed62e7609172534dea68b05f`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c075328080e6995af18ba0d46caacfb2d481e3bfd03bd1e1feb30c92ef355`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff40e518cab6103cc2dbbed344e68095afb68f480c2690b74900f7a7412e1ae9`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 22.8 MB (22756339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a62709feb8f58e8269a332f8cb621fcd984c1c3316283ccded16919bf71cda`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6acbdb8f48fcce734907c9a41f60cd59f358e65c812a3a4981f5e8b3276d52e`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1edc9932a94ae1c328f7a4190d5780f481b8890967cbc0e915a092e9a8f0871`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececc62a636024315de22ccaac302436c36e77452a38b7f08b83dca6b0795455`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 22.3 MB (22283301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.0.4-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:fa94327469822a56e83053ec60f804486fe9ee64c9f15be87233d2651926c32b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227933081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffec676bac1f14cd20f776a437da6b9fe135a587eb81263ff81adc16bb644ca6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 01:19:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:19:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 01:19:53 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 01:19:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 01:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 01:20:09 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 01:20:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 01:20:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 01:20:20 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 01:20:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243c89dd211d21587050138b4ba9caca0157449d59d6698f399bda8c9ac09647`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a64f1cb97b9459857deaad35fc7cb3146d6d807da8b42954f5570e8015ff8d`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 331.8 KB (331794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1ff6cf58cfc4c73c2c1cb14b2dbd5e91ccd8342cf3e7b4979f8c273605063b`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e961a01ad0f71ba1051d35d21755803b2fa1951fba5c545b345c4ddb497d4cf`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba307589781f303a1e20fe2f5c8a65fe379191b2f06f8de840ea2aaecf184f47`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 19.8 MB (19844611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb7ebad4ed4801f9cb8c8b750ab2454c93c826a400f3e5ac972a921b43dd3f2`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55c409429d09b5ed5634e52d87d957962d25ed1cd4d0dd5b62783cd4e2f446`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd36acd6048ee7eb5e37f47ea0ed75fb4bbcc90983346c92ae7cc8a3a43aa0a`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4383de892731480789dbba3ea542e0493a181b4619b7feb20fdd1701337750`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.7 MB (22748533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7686b51d722ad3222e89104c832b025336bd4a4a7c2beb26fa7eb95875deafbd`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cb46454301b3cc3fcacd9a425240920b39672c040ac885da807dfc3a33746f`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e72a7a6e8ddcef11a9b230a1cec67389895ec62572710f439e53ed43a59c019`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88569070dd26d817476810a2cd6ad26ea8f4e775ccdf912cbf72eef0203286a`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.3 MB (22270587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.4-windowsservercore-1809`

```console
$ docker pull docker@sha256:cc2efcf0a0bafa3c9df47a975aa3a6f095645104779c3b74fa0ff3ec9b2e1e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `docker:28.0.4-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:fa94327469822a56e83053ec60f804486fe9ee64c9f15be87233d2651926c32b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227933081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffec676bac1f14cd20f776a437da6b9fe135a587eb81263ff81adc16bb644ca6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 01:19:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:19:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 01:19:53 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 01:19:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 01:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 01:20:09 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 01:20:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 01:20:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 01:20:20 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 01:20:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243c89dd211d21587050138b4ba9caca0157449d59d6698f399bda8c9ac09647`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a64f1cb97b9459857deaad35fc7cb3146d6d807da8b42954f5570e8015ff8d`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 331.8 KB (331794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1ff6cf58cfc4c73c2c1cb14b2dbd5e91ccd8342cf3e7b4979f8c273605063b`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e961a01ad0f71ba1051d35d21755803b2fa1951fba5c545b345c4ddb497d4cf`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba307589781f303a1e20fe2f5c8a65fe379191b2f06f8de840ea2aaecf184f47`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 19.8 MB (19844611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb7ebad4ed4801f9cb8c8b750ab2454c93c826a400f3e5ac972a921b43dd3f2`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55c409429d09b5ed5634e52d87d957962d25ed1cd4d0dd5b62783cd4e2f446`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd36acd6048ee7eb5e37f47ea0ed75fb4bbcc90983346c92ae7cc8a3a43aa0a`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4383de892731480789dbba3ea542e0493a181b4619b7feb20fdd1701337750`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.7 MB (22748533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7686b51d722ad3222e89104c832b025336bd4a4a7c2beb26fa7eb95875deafbd`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cb46454301b3cc3fcacd9a425240920b39672c040ac885da807dfc3a33746f`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e72a7a6e8ddcef11a9b230a1cec67389895ec62572710f439e53ed43a59c019`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88569070dd26d817476810a2cd6ad26ea8f4e775ccdf912cbf72eef0203286a`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.3 MB (22270587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.4-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fe87151fca5614738a9a2377a76c82a06dcd81fa4827ccffb171958d6fb8494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `docker:28.0.4-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:0fe4c4d0f5c80021c50c85d104ea9454679f65eef396c515473415b2f3551677
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336245643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2260686200048a8ce26b4461ef2e6b0b73d9ce4353bad23921ebc2a3c91998b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:53:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:53:44 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:53:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:53:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:53:56 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:54:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:54:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:54:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd31ce4b72c969f090b09e0d47519bd245635b8a0766cad50a94e5285269e7f`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611d42417bb7b25c9cbe870a1d686b89d1d9756d80d42e4fd6e078d9f81ce4a`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 346.1 KB (346062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb06dc8ecf1b08f1190ad1c0d83e1fdabc1c8d67fc1ac6cb12116132b4f03468`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008480b629bc35e084765059b6f319dc7ff56f6ddd835cde71f710a1d1b3d636`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c50ac98d04810f7b347835e962e1cc758aeb4ba0ee8a7231139b95c1d2bde`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 19.9 MB (19852659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107085d17762a97b5dc8bd94314f73c5a529607173545e1afaca9a1d379c104d`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271fac6913f53452e4c148e110e15c1cf204cafbed62e7609172534dea68b05f`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c075328080e6995af18ba0d46caacfb2d481e3bfd03bd1e1feb30c92ef355`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff40e518cab6103cc2dbbed344e68095afb68f480c2690b74900f7a7412e1ae9`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 22.8 MB (22756339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a62709feb8f58e8269a332f8cb621fcd984c1c3316283ccded16919bf71cda`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6acbdb8f48fcce734907c9a41f60cd59f358e65c812a3a4981f5e8b3276d52e`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1edc9932a94ae1c328f7a4190d5780f481b8890967cbc0e915a092e9a8f0871`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececc62a636024315de22ccaac302436c36e77452a38b7f08b83dca6b0795455`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 22.3 MB (22283301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.0.4-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:7aacee74867dda438d28dbabea6db4a5d0891bc6ef5f0174dcd201910d0b3d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `docker:28.0.4-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8084d47f9c866ffb0fc6c74d818412ff1196f96066e4460f40ddb325112e0dcc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3460019679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8eb0a28181dcd66cffe910466b7bc06081957269945180b9e3be0f83af31bd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:39:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:39:26 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:39:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:39:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:39:39 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:39:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:39:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:39:50 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:39:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90663cbdd92914b16d1b360ec39197f6848f810c2e3d5f75368367b755fb29a5`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6859709f79778e74c7ef624e307d1930c0f780d10be536cb85d9893936b1d2`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 364.7 KB (364741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f3f9fb8993e6eddeb12b79a24923159ad4bba9c61def71fa12ee3f22eb949b`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b566c3c24e01288e140412f9834c019e4e2e71145ed6b6b079795f86b97424f2`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc5f946c4df03788d89b893a24b781d0bf21407cc2582ef5194f0eaea08db74`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 19.9 MB (19876882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2a3d26ad4275972b61ccdede64c0ddf0788bfa910b1275b74d172e5082198`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ad96060e962414395bc1991729228e8ca1e139d5b228efc120a55e2b9cab5`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb45857c62165be6ffbdcee3d0a6ae915dec7440305fc6ebfc274ca67879d0de`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946bf5bea56a89ae65bdacd4edde0517f360ff8ebcabd76df02411213a273c01`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.8 MB (22779634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6100d6c301fb149b342ede708f60d3cb8e10a3c1e9e3836c1baf34221724cef0`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d08118b8b7f3b7ff9643a05fa0fabf35417f346904745264b1b7878d575e1d`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8922e187bf58aaae3a9c3e2e9e8cfb6b00b0ad16a4e8cd5a47b91da0443a6`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93978eb25ad6c40ce8eccddc334dfe92007d5cc7ed7df32eaef8dd97ec678442`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.3 MB (22307251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:db3ecdf8e404584aa9c61124d4b94050a57baff6b22b6c24fd4306ba2ec0ee7f
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
$ docker pull docker@sha256:a6ea1ff707f785adb9be2f6e47e87700acf25028f2d9967d13b76431ea6df122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74014617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0289ff325f81264fd1a632fff7b28d944ff609ba51d8209663b51d4cbd458f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:a6169c645a49b492d6e68d672c3d1a916c2a8e4dd3c202c56fab0c1d2be6faaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ad129589ab4978d3da3e6ef2f6e3f4f5a0ac153762f2508d8f449b0a2ca999`

```dockerfile
```

-	Layers:
	-	`sha256:8c1f247b52e1e0f2bed9ae6eabd4518ca193f0085972b55c7d23a8898a174d70`  
		Last Modified: Thu, 10 Apr 2025 18:53:49 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:14eff0079ba0251493cf5982ca5b686ca7e1593b4e2cbb96c60123f917fe8d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68957297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b7b4e4a140075fe07f7d66321e2a97fdd546d69a162a7be5bc94d5798a42dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4fb6114e207be2cba4b2c019acb8be57897e196a2e6f4dc5d987772c0b43eaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab926911105f673368ef7c6dc6b1867f1ec4adcf7e3c4945ce3c1672996fd7fd`

```dockerfile
```

-	Layers:
	-	`sha256:ed38fd2f67937dcec97c17b94519db624b47e1988d2bbbd46b9f48eac203ad8b`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:12b3a15f36a8eb6cc92894f64cb1b50a6803355bc5304a3bd83dcc90bf5ad495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67969222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e080826ce1b653f01b7fb18b04d27924f0224e0be29ad901b75a2970050ca7b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:4afba38ec0f337734749f2c8b49e227a3d45f9f61389dbd68c9e7eecac222c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e89b56991dd0c0c1c8cbb2d9a7a7dc416f9f9f6b25120f4876559ffdb18d9`

```dockerfile
```

-	Layers:
	-	`sha256:279111cff860bea667d5c8682bb1a01b5bc0faf6cc7efd773554b9c7a12570c2`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:950fa733cdc541a5eaf180844e947417d625e7f1a5c2c2b11d739df98b7d0f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69756446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f62597355eb100013cdc808e76630be3420f850178b0bc0d90967c71a1c0852`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 10 Apr 2025 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 10 Apr 2025 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 10 Apr 2025 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Apr 2025 17:04:16 GMT
CMD ["sh"]
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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:39fd6f38aadc7c0729162941c92ea691ecabb023e6d976d71ceb673074ac230c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6643e2ca409745126713435320e0adac8ab3601ef2e01b647418f12ff740aea`

```dockerfile
```

-	Layers:
	-	`sha256:0640e53e70ef0e3d76844ae18c7b1d4b97d228264c700bcd5125ddfbd7443360`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:ddb0033088b4fab74881ade341a582e3c6c8021b82377703ba1a6106bd3ded44
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
$ docker pull docker@sha256:39c7ad73456a07cc38f6201542bb8fe90af7011bbfdeedd1a38d4073f231eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141196623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915daf53f2101bf4d33fd02a660d3380b7ae93c33353b8e89d490f88d99fe063`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:6fd9637e488f1aeddf77f0350669aab55ef3ba8513096467f7fdda49319b6aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c39104ed185c00634458eb4ac944cc4e3573157117d83049d13e426a8d9c82b`

```dockerfile
```

-	Layers:
	-	`sha256:d426f1591ec7aba06d77dfe270fc9e4bdf14a45b0dffdd3cc2e01d164c846f26`  
		Last Modified: Thu, 10 Apr 2025 19:01:36 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:f57bfe085889a95865995e69923b8c2d367e85ce52c02e8a7104749a580824ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131831229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0574bca6d6758ad673efce2f9b025494e66ba0f910eaa2d6b6595a8e4f6358b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2be501a51d4a1f0a576d79fbe13fe078b4bdbf776ed23cf879526ede3ef5e1`  
		Last Modified: Thu, 10 Apr 2025 19:00:55 GMT  
		Size: 7.0 MB (7036868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63997f7b0bbee48aec78071d1b0c603d44f66f2ea8b8d94000c1ecaf1c6104`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 89.9 KB (89861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7912ed8760d96518614159b4b19b70b895740d64c6f5fd05d096b33364737`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd81cb731158170a092369d294fde221053b50d8bbc81edbf3e97d07bc1fbb`  
		Last Modified: Thu, 10 Apr 2025 19:00:57 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb345ef49ff2d099926b4b83939cfa58a3a46fb13ba97090b378e589e8b520`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db539f3ab5ee441f7079488bcfebcbea706e544d414404b94bdbeb9346e2dfe`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:cbd722e549eb223a43ea7d493ead3354c85f66568db49c81d21988c69328147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dff5dcf2da2754b63daf44a1ef2835e410f441cd331f7acf9f2e7e2b5b87652`

```dockerfile
```

-	Layers:
	-	`sha256:378ab517d099321cd0621b9b29b751a08fefaa9b86368894c6a55e150d700860`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:1301cf6f282edbc7d94f178d2c0eec8394d27ef4583d71f8de15d7f3dd95dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130168775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a9103d3f83801d92a29c64c17850d951bec8b8d8ff10649c9ab13809b0a5a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aad6696717cc1615cc26f88fcafdff76f694a30eb5acf705c8363975f1e651`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 6.4 MB (6366036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245fa4cf98e8dd69566bc3e134d2fac91668df09f86fdcac3355d6694aa6191c`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 86.4 KB (86355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3167df5245a23cda38488a5fe3f8e58eb4176fb82896f6995ef46c98970c9`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f510c9deee4bcd5c38974dc46e0017e99e4725922e6e4946049c7d7107a47a`  
		Last Modified: Thu, 10 Apr 2025 19:00:48 GMT  
		Size: 55.7 MB (55741207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7919e15335d560caec91132a82a0dcc2d10952d51a073120aa793accc2651f`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24e3806a3f99ba66384d8e146985e86018b9652e0c3b7d6d6773fd939fda0b`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:7265de37982ade6cf359e6c152e6c05c89d4139cd11fcb5cf319ebc88b42497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8f79d22adc370d29acb203ab10dfe28d735a51e4ba15c1b1cbaae93c747b9b`

```dockerfile
```

-	Layers:
	-	`sha256:279933e04881d0f9dd131077fec7e0243e4fb68bd92873e62fa6b7791b84d285`  
		Last Modified: Thu, 10 Apr 2025 19:00:45 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7758019ffa34f3badc161535e37606309d838fe5dc8774ff95c6f8d03371be53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132551502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6bae33c1f057ecfe982e5da8ac6862fb24634b9f314179501611fb2812e53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e6c2bff16952f87dbf0660cbc7e3b894101e54070b72fe08f5ad6760ee0fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab359cbfa98deb3b443cef392d6076cd9cae3a5f443641500ac380c6c81ffe17`

```dockerfile
```

-	Layers:
	-	`sha256:466b4a3f5e33095850c5458dc8e94c486cb9cc628b450c8e203cd9d5fb180aae`  
		Last Modified: Thu, 10 Apr 2025 19:00:50 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:607d248e893dc10308b8f70afad4bf26cf166836856284c00c9971ec9d9e7dc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

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

### `docker:dind-rootless` - unknown; unknown

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

### `docker:dind-rootless` - linux; arm64 variant v8

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

### `docker:dind-rootless` - unknown; unknown

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

## `docker:latest`

```console
$ docker pull docker@sha256:ddb0033088b4fab74881ade341a582e3c6c8021b82377703ba1a6106bd3ded44
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
$ docker pull docker@sha256:39c7ad73456a07cc38f6201542bb8fe90af7011bbfdeedd1a38d4073f231eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141196623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915daf53f2101bf4d33fd02a660d3380b7ae93c33353b8e89d490f88d99fe063`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:6fd9637e488f1aeddf77f0350669aab55ef3ba8513096467f7fdda49319b6aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c39104ed185c00634458eb4ac944cc4e3573157117d83049d13e426a8d9c82b`

```dockerfile
```

-	Layers:
	-	`sha256:d426f1591ec7aba06d77dfe270fc9e4bdf14a45b0dffdd3cc2e01d164c846f26`  
		Last Modified: Thu, 10 Apr 2025 19:01:36 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:f57bfe085889a95865995e69923b8c2d367e85ce52c02e8a7104749a580824ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131831229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0574bca6d6758ad673efce2f9b025494e66ba0f910eaa2d6b6595a8e4f6358b5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
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
	-	`sha256:ee2bca0620c706293f4ca8d0cd608865c32790dbcfa82fcf15c6cf74a103d463`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 17.5 MB (17496767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6fba33178311aca4708ae365428e974572e47591a4ae577d77331ff88a06ce`  
		Last Modified: Tue, 25 Mar 2025 21:31:32 GMT  
		Size: 20.4 MB (20447100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4061c99fe7869ea2eb806c8a32a4195c6530392c36f20d86889c3d843a8b3`  
		Last Modified: Thu, 10 Apr 2025 18:53:30 GMT  
		Size: 19.7 MB (19668393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d1bdfdb3f97a760dbec9077225dc0381cbb6fb89cb745999d85ad047402d7`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f4349c727611c8db54c3839d22f5053326268d2e09f61b785d50b8fa0b4823`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4318507d0998b0a6cebd33365cfffd888e662f4503dd87a47d7eb8016348e7f9`  
		Last Modified: Thu, 10 Apr 2025 18:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2be501a51d4a1f0a576d79fbe13fe078b4bdbf776ed23cf879526ede3ef5e1`  
		Last Modified: Thu, 10 Apr 2025 19:00:55 GMT  
		Size: 7.0 MB (7036868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63997f7b0bbee48aec78071d1b0c603d44f66f2ea8b8d94000c1ecaf1c6104`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 89.9 KB (89861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7912ed8760d96518614159b4b19b70b895740d64c6f5fd05d096b33364737`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcd81cb731158170a092369d294fde221053b50d8bbc81edbf3e97d07bc1fbb`  
		Last Modified: Thu, 10 Apr 2025 19:00:57 GMT  
		Size: 55.7 MB (55741236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb345ef49ff2d099926b4b83939cfa58a3a46fb13ba97090b378e589e8b520`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db539f3ab5ee441f7079488bcfebcbea706e544d414404b94bdbeb9346e2dfe`  
		Last Modified: Thu, 10 Apr 2025 19:00:56 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:cbd722e549eb223a43ea7d493ead3354c85f66568db49c81d21988c69328147f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dff5dcf2da2754b63daf44a1ef2835e410f441cd331f7acf9f2e7e2b5b87652`

```dockerfile
```

-	Layers:
	-	`sha256:378ab517d099321cd0621b9b29b751a08fefaa9b86368894c6a55e150d700860`  
		Last Modified: Thu, 10 Apr 2025 19:00:54 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:1301cf6f282edbc7d94f178d2c0eec8394d27ef4583d71f8de15d7f3dd95dbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130168775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a9103d3f83801d92a29c64c17850d951bec8b8d8ff10649c9ab13809b0a5a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973e4d5e7b8a88f28ddf61a9c975a84d5c202e7c6ac4ee9bf3075ab3eee7cc1`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 7.3 MB (7301725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ac69f7dbe6571e755b2be383542fe4bcc20a4a163401b4cb37e24456db238`  
		Last Modified: Thu, 10 Apr 2025 18:53:18 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06115cba22cedd6a5e02bc92916e1637dd987588fa9afc2bbbc0a0bd5877c621`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 17.5 MB (17486315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b41ea82c0078f98e343e4b152218f1e2f48b53e27e9f52b410dd1211e712a51`  
		Last Modified: Thu, 10 Apr 2025 18:53:19 GMT  
		Size: 20.4 MB (20429561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5db0c2ba2635257bbca0d6db1b9ea6357558405fab53cca555f910276e784c`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 19.7 MB (19651344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6946a32d782273da91929941972d8fb6910cd62ca937487ad505a1a6f92fb`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04d536a8cd5e268bff63c8a0e66ce2366f85676d51fc1923dfcadb466d3b68`  
		Last Modified: Thu, 10 Apr 2025 18:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a775b65b653c99f6d55f9037231ed68ba0a057eb017f31b363297f0607389d0a`  
		Last Modified: Thu, 10 Apr 2025 18:53:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aad6696717cc1615cc26f88fcafdff76f694a30eb5acf705c8363975f1e651`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 6.4 MB (6366036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245fa4cf98e8dd69566bc3e134d2fac91668df09f86fdcac3355d6694aa6191c`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 86.4 KB (86355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3167df5245a23cda38488a5fe3f8e58eb4176fb82896f6995ef46c98970c9`  
		Last Modified: Thu, 10 Apr 2025 19:00:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f510c9deee4bcd5c38974dc46e0017e99e4725922e6e4946049c7d7107a47a`  
		Last Modified: Thu, 10 Apr 2025 19:00:48 GMT  
		Size: 55.7 MB (55741207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7919e15335d560caec91132a82a0dcc2d10952d51a073120aa793accc2651f`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24e3806a3f99ba66384d8e146985e86018b9652e0c3b7d6d6773fd939fda0b`  
		Last Modified: Thu, 10 Apr 2025 19:00:47 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:7265de37982ade6cf359e6c152e6c05c89d4139cd11fcb5cf319ebc88b42497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8f79d22adc370d29acb203ab10dfe28d735a51e4ba15c1b1cbaae93c747b9b`

```dockerfile
```

-	Layers:
	-	`sha256:279933e04881d0f9dd131077fec7e0243e4fb68bd92873e62fa6b7791b84d285`  
		Last Modified: Thu, 10 Apr 2025 19:00:45 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7758019ffa34f3badc161535e37606309d838fe5dc8774ff95c6f8d03371be53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132551502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6bae33c1f057ecfe982e5da8ac6862fb24634b9f314179501611fb2812e53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_VERSION=28.0.4
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 27 Mar 2025 11:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD ["sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 27 Mar 2025 11:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 11:04:16 GMT
VOLUME [/var/lib/docker]
# Thu, 27 Mar 2025 11:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 27 Mar 2025 11:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 27 Mar 2025 11:04:16 GMT
CMD []
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

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:e6c2bff16952f87dbf0660cbc7e3b894101e54070b72fe08f5ad6760ee0fa090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab359cbfa98deb3b443cef392d6076cd9cae3a5f443641500ac380c6c81ffe17`

```dockerfile
```

-	Layers:
	-	`sha256:466b4a3f5e33095850c5458dc8e94c486cb9cc628b450c8e203cd9d5fb180aae`  
		Last Modified: Thu, 10 Apr 2025 19:00:50 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:b4976a3b828001015b15b82f7164b772b541d63c40ff57d25001d0a654e09e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8084d47f9c866ffb0fc6c74d818412ff1196f96066e4460f40ddb325112e0dcc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3460019679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8eb0a28181dcd66cffe910466b7bc06081957269945180b9e3be0f83af31bd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:39:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:39:26 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:39:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:39:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:39:39 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:39:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:39:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:39:50 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:39:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90663cbdd92914b16d1b360ec39197f6848f810c2e3d5f75368367b755fb29a5`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6859709f79778e74c7ef624e307d1930c0f780d10be536cb85d9893936b1d2`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 364.7 KB (364741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f3f9fb8993e6eddeb12b79a24923159ad4bba9c61def71fa12ee3f22eb949b`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b566c3c24e01288e140412f9834c019e4e2e71145ed6b6b079795f86b97424f2`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc5f946c4df03788d89b893a24b781d0bf21407cc2582ef5194f0eaea08db74`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 19.9 MB (19876882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2a3d26ad4275972b61ccdede64c0ddf0788bfa910b1275b74d172e5082198`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ad96060e962414395bc1991729228e8ca1e139d5b228efc120a55e2b9cab5`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb45857c62165be6ffbdcee3d0a6ae915dec7440305fc6ebfc274ca67879d0de`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946bf5bea56a89ae65bdacd4edde0517f360ff8ebcabd76df02411213a273c01`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.8 MB (22779634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6100d6c301fb149b342ede708f60d3cb8e10a3c1e9e3836c1baf34221724cef0`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d08118b8b7f3b7ff9643a05fa0fabf35417f346904745264b1b7878d575e1d`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8922e187bf58aaae3a9c3e2e9e8cfb6b00b0ad16a4e8cd5a47b91da0443a6`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93978eb25ad6c40ce8eccddc334dfe92007d5cc7ed7df32eaef8dd97ec678442`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.3 MB (22307251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:0fe4c4d0f5c80021c50c85d104ea9454679f65eef396c515473415b2f3551677
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336245643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2260686200048a8ce26b4461ef2e6b0b73d9ce4353bad23921ebc2a3c91998b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:53:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:53:44 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:53:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:53:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:53:56 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:54:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:54:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:54:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd31ce4b72c969f090b09e0d47519bd245635b8a0766cad50a94e5285269e7f`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611d42417bb7b25c9cbe870a1d686b89d1d9756d80d42e4fd6e078d9f81ce4a`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 346.1 KB (346062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb06dc8ecf1b08f1190ad1c0d83e1fdabc1c8d67fc1ac6cb12116132b4f03468`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008480b629bc35e084765059b6f319dc7ff56f6ddd835cde71f710a1d1b3d636`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c50ac98d04810f7b347835e962e1cc758aeb4ba0ee8a7231139b95c1d2bde`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 19.9 MB (19852659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107085d17762a97b5dc8bd94314f73c5a529607173545e1afaca9a1d379c104d`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271fac6913f53452e4c148e110e15c1cf204cafbed62e7609172534dea68b05f`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c075328080e6995af18ba0d46caacfb2d481e3bfd03bd1e1feb30c92ef355`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff40e518cab6103cc2dbbed344e68095afb68f480c2690b74900f7a7412e1ae9`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 22.8 MB (22756339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a62709feb8f58e8269a332f8cb621fcd984c1c3316283ccded16919bf71cda`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6acbdb8f48fcce734907c9a41f60cd59f358e65c812a3a4981f5e8b3276d52e`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1edc9932a94ae1c328f7a4190d5780f481b8890967cbc0e915a092e9a8f0871`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececc62a636024315de22ccaac302436c36e77452a38b7f08b83dca6b0795455`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 22.3 MB (22283301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:fa94327469822a56e83053ec60f804486fe9ee64c9f15be87233d2651926c32b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227933081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffec676bac1f14cd20f776a437da6b9fe135a587eb81263ff81adc16bb644ca6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 01:19:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:19:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 01:19:53 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 01:19:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 01:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 01:20:09 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 01:20:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 01:20:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 01:20:20 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 01:20:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243c89dd211d21587050138b4ba9caca0157449d59d6698f399bda8c9ac09647`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a64f1cb97b9459857deaad35fc7cb3146d6d807da8b42954f5570e8015ff8d`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 331.8 KB (331794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1ff6cf58cfc4c73c2c1cb14b2dbd5e91ccd8342cf3e7b4979f8c273605063b`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e961a01ad0f71ba1051d35d21755803b2fa1951fba5c545b345c4ddb497d4cf`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba307589781f303a1e20fe2f5c8a65fe379191b2f06f8de840ea2aaecf184f47`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 19.8 MB (19844611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb7ebad4ed4801f9cb8c8b750ab2454c93c826a400f3e5ac972a921b43dd3f2`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55c409429d09b5ed5634e52d87d957962d25ed1cd4d0dd5b62783cd4e2f446`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd36acd6048ee7eb5e37f47ea0ed75fb4bbcc90983346c92ae7cc8a3a43aa0a`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4383de892731480789dbba3ea542e0493a181b4619b7feb20fdd1701337750`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.7 MB (22748533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7686b51d722ad3222e89104c832b025336bd4a4a7c2beb26fa7eb95875deafbd`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cb46454301b3cc3fcacd9a425240920b39672c040ac885da807dfc3a33746f`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e72a7a6e8ddcef11a9b230a1cec67389895ec62572710f439e53ed43a59c019`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88569070dd26d817476810a2cd6ad26ea8f4e775ccdf912cbf72eef0203286a`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.3 MB (22270587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:cc2efcf0a0bafa3c9df47a975aa3a6f095645104779c3b74fa0ff3ec9b2e1e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:fa94327469822a56e83053ec60f804486fe9ee64c9f15be87233d2651926c32b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227933081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffec676bac1f14cd20f776a437da6b9fe135a587eb81263ff81adc16bb644ca6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 01:19:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:19:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 01:19:53 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 01:19:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 01:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 01:20:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 01:20:09 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 01:20:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:20:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 01:20:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 01:20:20 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 01:20:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243c89dd211d21587050138b4ba9caca0157449d59d6698f399bda8c9ac09647`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a64f1cb97b9459857deaad35fc7cb3146d6d807da8b42954f5570e8015ff8d`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 331.8 KB (331794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1ff6cf58cfc4c73c2c1cb14b2dbd5e91ccd8342cf3e7b4979f8c273605063b`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e961a01ad0f71ba1051d35d21755803b2fa1951fba5c545b345c4ddb497d4cf`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba307589781f303a1e20fe2f5c8a65fe379191b2f06f8de840ea2aaecf184f47`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 19.8 MB (19844611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb7ebad4ed4801f9cb8c8b750ab2454c93c826a400f3e5ac972a921b43dd3f2`  
		Last Modified: Wed, 09 Apr 2025 01:20:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55c409429d09b5ed5634e52d87d957962d25ed1cd4d0dd5b62783cd4e2f446`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd36acd6048ee7eb5e37f47ea0ed75fb4bbcc90983346c92ae7cc8a3a43aa0a`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4383de892731480789dbba3ea542e0493a181b4619b7feb20fdd1701337750`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.7 MB (22748533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7686b51d722ad3222e89104c832b025336bd4a4a7c2beb26fa7eb95875deafbd`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cb46454301b3cc3fcacd9a425240920b39672c040ac885da807dfc3a33746f`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e72a7a6e8ddcef11a9b230a1cec67389895ec62572710f439e53ed43a59c019`  
		Last Modified: Wed, 09 Apr 2025 01:20:30 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88569070dd26d817476810a2cd6ad26ea8f4e775ccdf912cbf72eef0203286a`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 22.3 MB (22270587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0fe87151fca5614738a9a2377a76c82a06dcd81fa4827ccffb171958d6fb8494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:0fe4c4d0f5c80021c50c85d104ea9454679f65eef396c515473415b2f3551677
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336245643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2260686200048a8ce26b4461ef2e6b0b73d9ce4353bad23921ebc2a3c91998b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:53:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:53:44 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:53:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:53:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:53:56 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:54:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:54:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:54:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd31ce4b72c969f090b09e0d47519bd245635b8a0766cad50a94e5285269e7f`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611d42417bb7b25c9cbe870a1d686b89d1d9756d80d42e4fd6e078d9f81ce4a`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 346.1 KB (346062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb06dc8ecf1b08f1190ad1c0d83e1fdabc1c8d67fc1ac6cb12116132b4f03468`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008480b629bc35e084765059b6f319dc7ff56f6ddd835cde71f710a1d1b3d636`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c50ac98d04810f7b347835e962e1cc758aeb4ba0ee8a7231139b95c1d2bde`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 19.9 MB (19852659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107085d17762a97b5dc8bd94314f73c5a529607173545e1afaca9a1d379c104d`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271fac6913f53452e4c148e110e15c1cf204cafbed62e7609172534dea68b05f`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c075328080e6995af18ba0d46caacfb2d481e3bfd03bd1e1feb30c92ef355`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff40e518cab6103cc2dbbed344e68095afb68f480c2690b74900f7a7412e1ae9`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 22.8 MB (22756339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a62709feb8f58e8269a332f8cb621fcd984c1c3316283ccded16919bf71cda`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6acbdb8f48fcce734907c9a41f60cd59f358e65c812a3a4981f5e8b3276d52e`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1edc9932a94ae1c328f7a4190d5780f481b8890967cbc0e915a092e9a8f0871`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececc62a636024315de22ccaac302436c36e77452a38b7f08b83dca6b0795455`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 22.3 MB (22283301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:7aacee74867dda438d28dbabea6db4a5d0891bc6ef5f0174dcd201910d0b3d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8084d47f9c866ffb0fc6c74d818412ff1196f96066e4460f40ddb325112e0dcc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3460019679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8eb0a28181dcd66cffe910466b7bc06081957269945180b9e3be0f83af31bd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:39:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:39:26 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:39:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:39:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:39:39 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:39:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:39:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:39:50 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:39:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90663cbdd92914b16d1b360ec39197f6848f810c2e3d5f75368367b755fb29a5`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6859709f79778e74c7ef624e307d1930c0f780d10be536cb85d9893936b1d2`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 364.7 KB (364741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f3f9fb8993e6eddeb12b79a24923159ad4bba9c61def71fa12ee3f22eb949b`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b566c3c24e01288e140412f9834c019e4e2e71145ed6b6b079795f86b97424f2`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc5f946c4df03788d89b893a24b781d0bf21407cc2582ef5194f0eaea08db74`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 19.9 MB (19876882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2a3d26ad4275972b61ccdede64c0ddf0788bfa910b1275b74d172e5082198`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ad96060e962414395bc1991729228e8ca1e139d5b228efc120a55e2b9cab5`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb45857c62165be6ffbdcee3d0a6ae915dec7440305fc6ebfc274ca67879d0de`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946bf5bea56a89ae65bdacd4edde0517f360ff8ebcabd76df02411213a273c01`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.8 MB (22779634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6100d6c301fb149b342ede708f60d3cb8e10a3c1e9e3836c1baf34221724cef0`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d08118b8b7f3b7ff9643a05fa0fabf35417f346904745264b1b7878d575e1d`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8922e187bf58aaae3a9c3e2e9e8cfb6b00b0ad16a4e8cd5a47b91da0443a6`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93978eb25ad6c40ce8eccddc334dfe92007d5cc7ed7df32eaef8dd97ec678442`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.3 MB (22307251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

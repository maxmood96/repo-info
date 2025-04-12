## `docker:rc`

```console
$ docker pull docker@sha256:b0016f62aac43cd8d6cdeeb2b5ca7f5b3594e53d52a57ab9496c7edabfc1855e
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

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:1c1f3631c4eaf235e28e2c4321e8d06ea76c4cb00ac4bbf1e9d64ddbae7ed3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141214688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76723f4a84126c05a35865da395139101f9a1308fed9e389831f10926b21c73`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Apr 2025 22:41:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
CMD ["sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Apr 2025 22:41:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c2912c6674b780de69d80fd6c953056ae87eaa82dd759bc7ba21b5f0ac8f97`  
		Last Modified: Sat, 12 Apr 2025 00:49:42 GMT  
		Size: 8.1 MB (8062938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033636702f1a3e425825bd8ec7c1577db833ddc18f805f20922d425cc9a5f421`  
		Last Modified: Sat, 12 Apr 2025 00:49:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9889ead0a67fcb7983beb2ab5e5e16c5e24819f23b0ac92222cb76841607f2`  
		Last Modified: Sat, 12 Apr 2025 00:49:42 GMT  
		Size: 19.6 MB (19559040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3418dfb8da310ab6516518f3cc1388cebfc5155c807e88bb883050acae79bbbe`  
		Last Modified: Sat, 12 Apr 2025 00:49:42 GMT  
		Size: 21.8 MB (21848956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f16efb7f2e0c496cdd788bc06714527af4275a97c8a7fe87cd760372ceca4`  
		Last Modified: Sat, 12 Apr 2025 00:49:43 GMT  
		Size: 20.9 MB (20915269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0e2126d73969b528b3810acb908dbf48aed9d8d03588ba4f4e0de9b83db324`  
		Last Modified: Sat, 12 Apr 2025 00:49:43 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac634fc42755229105796d50d926edd50e4c6a4b4c13ff375694cfa27c65fd20`  
		Last Modified: Sat, 12 Apr 2025 00:49:43 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb67065fadb00476ff46805f50b70b9abf4a375ffa249013a3a3db4a3deecd07`  
		Last Modified: Sat, 12 Apr 2025 00:49:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea147eb53749828940955bffe726ed8ddb1571efea2cc5d0d8e3599ee2cefa11`  
		Last Modified: Sat, 12 Apr 2025 01:07:53 GMT  
		Size: 6.7 MB (6733021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ac24bef75fc04cc4a07c4f47132f2b85e9e77871ff8a64413ddcdd8ea659b9`  
		Last Modified: Sat, 12 Apr 2025 01:07:53 GMT  
		Size: 90.3 KB (90333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cf4cd4dd7856a50d8d218abc0dcc4d6eacc01e7e9084be3c62c2896fcf5f1f`  
		Last Modified: Sat, 12 Apr 2025 01:07:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a397883ecde8827a9603d18e4c2e1225504ff5b5d475ff5457045db2824bb6c7`  
		Last Modified: Sat, 12 Apr 2025 01:07:53 GMT  
		Size: 60.4 MB (60354770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66257864e2df66b2bbba5a12e0984fc022086f86071afe6c978f1f293ed2dd4`  
		Last Modified: Sat, 12 Apr 2025 01:07:53 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39e839fffbbed44a6fb9157858b9ec223bf000baebe474bc5a8d8dfc091b022`  
		Last Modified: Sat, 12 Apr 2025 01:07:54 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:92681abc07c265efb016d3440b271366971be83ff51a7ecf95489314343fc886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1dcb47176b80941041f7f088c0f9e6e65ea54e3a5798307c0bdc2a55f0b09ba`

```dockerfile
```

-	Layers:
	-	`sha256:d4b64963846c3fc42544d27ddfeb43d679e8d6c04ba68ad55aec7257c5a3a378`  
		Last Modified: Sat, 12 Apr 2025 01:07:52 GMT  
		Size: 34.1 KB (34115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v6

```console
$ docker pull docker@sha256:81d8f7847f6eea8bce407eec82bb816bb720118e2251c05a667960c2ae0041a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131852359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ece38db521a337214e272e57bce9ee03c52faaaf2537340105916cd21be7ff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Apr 2025 22:41:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
CMD ["sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Apr 2025 22:41:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
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
	-	`sha256:6bcffdb45e1d7a9f5156ba913d5ff567b2d61badd19fdc009929b485b93127c5`  
		Last Modified: Sat, 12 Apr 2025 00:49:15 GMT  
		Size: 17.5 MB (17507801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5302747227ebed962d78feec2788d6371dc5e25e77dcc24e5d59fa3ecaadb12`  
		Last Modified: Sat, 12 Apr 2025 00:49:15 GMT  
		Size: 20.4 MB (20447108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4637be1670aca6c4344873723f0bf0d239a9d1f537e1da66fe7fa67fc1cccf12`  
		Last Modified: Sat, 12 Apr 2025 00:49:15 GMT  
		Size: 19.7 MB (19668394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9da5a1e08496c0a71c6a21e0067850a5750e60356ca9834371770bf478f106`  
		Last Modified: Sat, 12 Apr 2025 00:49:14 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05744f329b00974dbe900c0590ffc34885ef78fdd537c4a698c1454aa2dba5b1`  
		Last Modified: Sat, 12 Apr 2025 00:49:16 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f1e3219b4b1635fa51b55e3afec71c63938c69233f0b3d6e39e0eb94c53c5a`  
		Last Modified: Sat, 12 Apr 2025 00:49:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556c2e6a09badf3d1e834a922e92dee5c0e9b1cb142cf10dd50e20323a51467a`  
		Last Modified: Sat, 12 Apr 2025 01:07:26 GMT  
		Size: 7.0 MB (7036875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7434cf75fa2b282d12c4f452b5310751ef4fa097aa6fa80b00a4f6e93b2dd23`  
		Last Modified: Sat, 12 Apr 2025 01:07:25 GMT  
		Size: 89.9 KB (89869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd88cea9a36cc98fb7514fd1d84c2ce6677d2def32993bca52e1390c002509c5`  
		Last Modified: Sat, 12 Apr 2025 01:07:25 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0e5bb55cb1462bd614e29134133c7290b6a59d9221fd9261ce11ae273ba094`  
		Last Modified: Sat, 12 Apr 2025 01:07:28 GMT  
		Size: 55.8 MB (55751325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a05092ead46e1d931531430d453eb286bbb75fb36912cbfbc532b57ea6ca85`  
		Last Modified: Sat, 12 Apr 2025 01:07:26 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff2dc6f93c830b60c5875ba508f280c6f91c67f55be609880ec4aa371e4995b`  
		Last Modified: Sat, 12 Apr 2025 01:07:26 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:2e6d2335793285a759758c2859021333db9b0ba51b84debb8a3b271919fdcad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6eebacf92edb122b4c3a3411316ee68fded78a06d23eee42cc8e0646af7508`

```dockerfile
```

-	Layers:
	-	`sha256:ef67a005b1a87a1b12f2e675f490ad9e66164478c404f9d880dc11f82c2aa33c`  
		Last Modified: Sat, 12 Apr 2025 01:07:25 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v7

```console
$ docker pull docker@sha256:31c6faa0c2d1d4b27fd97ba02ac63f15f9d6569b3df51b29d3a9e81ca08ce0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130187298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeeb62df991f3b3eb2c46fe2d977dde6a9ee6df670858ac72214236bc62c1e93`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Apr 2025 22:41:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
CMD ["sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Apr 2025 22:41:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7a863941b474a506f4edb3f5adaf1e200e40756e9de8fe65d4d36562b25504`  
		Last Modified: Sat, 12 Apr 2025 00:49:37 GMT  
		Size: 7.3 MB (7301726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86813364942079d0961301d10f4e92acd159c58618730aac879a340839991ae9`  
		Last Modified: Sat, 12 Apr 2025 00:49:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f394f66e057299ef71b46e7744acbd9a6b45f5dd0e8c07bb6ae1e8d425719c4`  
		Last Modified: Sat, 12 Apr 2025 00:49:38 GMT  
		Size: 17.5 MB (17494739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac071605d32b72f48346a268add4daade0ea5aea92d2915621cfccf850764d2`  
		Last Modified: Sat, 12 Apr 2025 00:49:38 GMT  
		Size: 20.4 MB (20429554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4575ea7c9bfb6f78490e18e90a8a95cc05769affa29dbf65aa9cbea99d88ac4`  
		Last Modified: Sat, 12 Apr 2025 00:49:38 GMT  
		Size: 19.7 MB (19651321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbbae29b0fec32ec679e393f8f49e5021fccbc5a3ea0764247a316d57b2474c`  
		Last Modified: Sat, 12 Apr 2025 00:49:38 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa87ad97b3e8aeaf65c84af08f770cf426705530f7c248d713aeec8b6d92182`  
		Last Modified: Sat, 12 Apr 2025 00:49:39 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20136b9d6c249108ce5dc7e78a057cd21c644530216c8f8b3629aa68b2ba1abc`  
		Last Modified: Sat, 12 Apr 2025 00:49:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7e55c240f36ddd7c7a2774a2476a87fe1f71107a140aff853515bea055a68c`  
		Last Modified: Sat, 12 Apr 2025 01:07:26 GMT  
		Size: 6.4 MB (6366063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096fd5f8790c667583892841f4e03c206e1e43200eeeff8a65f86a2623a54cf4`  
		Last Modified: Sat, 12 Apr 2025 01:07:26 GMT  
		Size: 86.3 KB (86346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1150665321b72c546caab4836888c7ce3c41d435536134fba9a7dd09e2fef4`  
		Last Modified: Sat, 12 Apr 2025 01:07:26 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bbc09eb79413954f924c5886903940f5392b575db7a9950c24ed96353493b`  
		Last Modified: Sat, 12 Apr 2025 01:07:28 GMT  
		Size: 55.8 MB (55751311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0c559921575e369c5a73d53e60c94132087916ea74c2f1297d2b394427a8ef`  
		Last Modified: Sat, 12 Apr 2025 01:07:27 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ee3cae2a5f7344225bc06ace39d41e88443fbb592e5aca6b0e6f7d4dcb94e`  
		Last Modified: Sat, 12 Apr 2025 01:07:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:278e9b4fe2017e60b4a8f03e6338caf2a10265584091262589cc1c63e8862d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa9a0690d60b0724d7813af676998cd34d87925f136b7c451798c4c0413d737`

```dockerfile
```

-	Layers:
	-	`sha256:ebff9974170aa0e7d0dc81017dc51c1721106b9d94f12d82ed435a2022ad985c`  
		Last Modified: Sat, 12 Apr 2025 01:07:25 GMT  
		Size: 34.3 KB (34274 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:84c0c0c685e1c6f8a3becb78b8204dbefc1af7de964dfe436759df743ddcb123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132570266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a349411c973c2906078501e40618d0ec35dfe42d1bd2ea8793a9f994d8d75f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-amd64'; 			sha256='805195386fba0cea5a1487cf0d47da82a145ea0a792bd3fb477583e2dbcdcc2f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v6'; 			sha256='24307aab46799cee78af26f3de11e82f029e6bbf36ece9b09335dbcebbca8bc7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm-v7'; 			sha256='de55bb6389524edd0b707d4ff63118e63ec015379e3e4daf94ca6127878dbe04'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-arm64'; 			sha256='6e9e455b5ec1c7ac708f2640a86c5cecce38c72e48acff6cb219dfdfa2dda781'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-ppc64le'; 			sha256='f47d600506783d9ee47bfca3287fdeb17123ac59c5a046393bd5cacb3050d1b5'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-riscv64'; 			sha256='812cffddafac44c0ff7a86221c321763c49a32ea65e1194ef489ba1ef5e47e70'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.linux-s390x'; 			sha256='bfc6cfb663d1b6e2ed6ff1bf0f820024eac67145d29cb33cb24790b18f23fff4'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-x86_64'; 			sha256='dba1915cf2f282527f5df0cd7a94b9503047ed200317801853abe8f22c8cd493'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv6'; 			sha256='e7ea8760cb2b20808bdea94b15bccdd91b80045e3f0ae9efb7d4082ea1b98328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-armv7'; 			sha256='9f9831ef951fbb1eaff7dfd17e4ca2e3522a9e66670e81075b68a25fbbfc0ee2'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-aarch64'; 			sha256='a08457d837d5d4ed7c079f0721dc51ef3f21ce2d9654a6abd44944b74d975cd2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-ppc64le'; 			sha256='7dfe56cde21ae0d4b96083629b5142b1f00b51baf6d3a695c0ac700822175b13'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-riscv64'; 			sha256='85ecd8c7ff0218a3b66a4ddcc3ef66d28b26ce9ec310531b56416cb8d6304b03'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-linux-s390x'; 			sha256='f9bc89ad8d048690f3cba9c05df5bddd9d0f5dcb03bfd41ceb613d7e560a76a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Apr 2025 22:41:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
CMD ["sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 11 Apr 2025 22:41:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 11 Apr 2025 22:41:23 GMT
VOLUME [/var/lib/docker]
# Fri, 11 Apr 2025 22:41:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 11 Apr 2025 22:41:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 11 Apr 2025 22:41:23 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fec373c1d0474f24abdc9ce93334431770a3b0209971d0929e73ed22d85ecbc`  
		Last Modified: Sat, 12 Apr 2025 00:49:02 GMT  
		Size: 8.1 MB (8077227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d52d26e738e43cfbcd8abf247a5253f9f3aae09891f71d64b4e43e51d3d0bfd`  
		Last Modified: Sat, 12 Apr 2025 00:49:02 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc0a22b7c4395eb457df1cf4c0d1406f18c8fc854e4f53d74e902d2a6f6eb31`  
		Last Modified: Sat, 12 Apr 2025 00:49:03 GMT  
		Size: 18.5 MB (18472339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aa4f1ae74e95c1e7b93333c9c56591c191323951e125fddc307aab2bf9c75b`  
		Last Modified: Sat, 12 Apr 2025 00:49:03 GMT  
		Size: 20.1 MB (20061170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bf4661c7c6265578c119157b20ab6968f53eba5fc741dc6652b392ab9387d1`  
		Last Modified: Sat, 12 Apr 2025 00:49:04 GMT  
		Size: 19.2 MB (19165680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f639fff06f25dcd6c2fe5a0b8cb90cf1ca9c9df99a421cf8bace34e34ac72f`  
		Last Modified: Sat, 12 Apr 2025 00:49:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fa0168b6d5ba8b7bf7e0daf4fa95214787f41e38e0bc81197247f52f151606`  
		Last Modified: Sat, 12 Apr 2025 00:49:04 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec167bf5547b5753ee4781f015faeb4567f1b1f19236b0a0ec6aef550f13e47`  
		Last Modified: Sat, 12 Apr 2025 00:49:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a5d9149dcd9d9d3617f4351a7ffb2d38afdda24ba2b931283088a2cab5b829`  
		Last Modified: Sat, 12 Apr 2025 01:07:26 GMT  
		Size: 7.0 MB (6978785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcc8e278b3792e72980cc97241aa8e444a9437cffa44d8e45f8cce6d735981c`  
		Last Modified: Sat, 12 Apr 2025 01:07:26 GMT  
		Size: 99.4 KB (99394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31e1f42d6ea45a1c9f7fd63420094aa2115a8f56ca351f07b25e9aa49922fe0`  
		Last Modified: Sat, 12 Apr 2025 01:07:26 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc0ae71b0e3aee391c6ee31bc7d7dfa25997161028a59ba7b030d0ef2a91106`  
		Last Modified: Sat, 12 Apr 2025 01:07:28 GMT  
		Size: 55.7 MB (55714533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1ffc06c7dee7d02ceeca16c7f13ac04ef5fdd28c9512311d9688f4e317267b`  
		Last Modified: Sat, 12 Apr 2025 01:07:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687f4405294f296faabf0c3b42548227e90d3c4ab3ac0a5fecec3fdc693adcf`  
		Last Modified: Sat, 12 Apr 2025 01:07:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:10f5d2bf68787e4fa1827f1999521ae896b3020d241557fa6ee97cb2668b0073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cf58b16d67bc4df12d6a345719b8caeb1d0b8458fb6383dd35223994d782c7`

```dockerfile
```

-	Layers:
	-	`sha256:47b890bb6be3d3f9a10a5ec5c4a93cb96aeb643191c167e3db515a1b84eb9099`  
		Last Modified: Sat, 12 Apr 2025 01:07:25 GMT  
		Size: 34.3 KB (34327 bytes)  
		MIME: application/vnd.in-toto+json

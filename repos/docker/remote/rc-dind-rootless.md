## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:635e70bcc202141bfb0129f6b0c039f7dbe54a17fbbe658e22dd1f28c0da5224
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:bfc13b1cf98598d7e65b8e1cc985950ea9157d8167a7687ef58e643eb22ac748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156103901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eaf7fe9418ee9995bf18edb9c473b5771e4d2f2570cb3337022a0f69cc773a0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 18:52:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENV DOCKER_VERSION=27.5.0-rc.2
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Jan 2025 18:52:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Jan 2025 18:52:25 GMT
CMD ["sh"]
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Jan 2025 18:52:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Jan 2025 18:52:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Jan 2025 18:52:25 GMT
CMD []
# Wed, 08 Jan 2025 18:52:25 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.5.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.5.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 08 Jan 2025 18:52:25 GMT
USER rootless
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9da8d98be9c497538e046636271095d60600736b8b98dd17d89b85cf6750a8f`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 8.1 MB (8058734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4386589b6f3f3d4248a89850307f7fce69767219761e159ae96376e95133648c`  
		Last Modified: Thu, 09 Jan 2025 22:28:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eec89dde7ca9124d2c1f9aad8c5610b044c03e8375a50440e2b400c0b684dbf`  
		Last Modified: Thu, 09 Jan 2025 22:28:47 GMT  
		Size: 18.8 MB (18849789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621d9e9d8f1c084324a9bfc17effabc710a3142456efbde84cc52357b5d39c7a`  
		Last Modified: Thu, 09 Jan 2025 22:28:47 GMT  
		Size: 18.8 MB (18798855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b891fc60d0f0b3357554b2556dcc95eda57ad9cab9cefea2dd40d3fbfe313`  
		Last Modified: Thu, 09 Jan 2025 22:28:47 GMT  
		Size: 19.3 MB (19308691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b8e858f3681e6fef39f2adbdfcaeaaf4d540cbf7142ddfd213872e305aa38a`  
		Last Modified: Thu, 09 Jan 2025 22:28:47 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33046038b891c90630e087369904e988fa6618edaa3a614ad802c2d6f5fbac02`  
		Last Modified: Thu, 09 Jan 2025 22:28:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639543bd8ef1632e940a6cba7fe057e640d898242a0b129845132d3be23fafe5`  
		Last Modified: Thu, 09 Jan 2025 22:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace27fa9e4639610a287679ddc2bf0f03ba14694919d2fe582df612d4b935ced`  
		Last Modified: Thu, 09 Jan 2025 23:10:07 GMT  
		Size: 6.7 MB (6733343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd8af51b9660f3a658192e72db4dd4386cfd35568040e3cf910f3d9549285d1`  
		Last Modified: Thu, 09 Jan 2025 23:10:07 GMT  
		Size: 89.4 KB (89424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819093b9d5d75bf946e514cbf01f4f09b40207f9fd8a7ac1f110b147c14dd613`  
		Last Modified: Thu, 09 Jan 2025 23:10:07 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b54d318c2a3207b6136045fe7075c1698d17b251bd5494282cb079f8bcc25c3`  
		Last Modified: Thu, 09 Jan 2025 23:10:09 GMT  
		Size: 58.3 MB (58323615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db98cab4ad3ea3d0eb1af945eeede03d4f0ccf774b4820f7ed870a2f91a86ba`  
		Last Modified: Thu, 09 Jan 2025 23:10:08 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0dcaad9234f8b6ce617834af3e63b0a0b42c20deab8944c0a3e5bcf588a32c`  
		Last Modified: Thu, 09 Jan 2025 23:10:08 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d456e4cdc51d1a39608322481059fc82ced4194c5491c1b2ed7f2409ad456099`  
		Last Modified: Fri, 10 Jan 2025 00:07:40 GMT  
		Size: 986.6 KB (986566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174453cf65807e013df1a93150bfdbcbd81521d64fa27707d80f6f58ac66df8a`  
		Last Modified: Fri, 10 Jan 2025 00:07:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a94c1ee5081fd19768e52959bef47551717dfaf424e3d04c1c64a2cfcc3dc9`  
		Last Modified: Fri, 10 Jan 2025 00:07:40 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0acda83b1ec9e63563d84234e843213f3c2ff2294d41904cd635a9995003a52`  
		Last Modified: Fri, 10 Jan 2025 00:07:41 GMT  
		Size: 21.3 MB (21303871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9978f4167e51d63e270863c9f64f807a03e7ad7348fa5a43cd266b62200b86`  
		Last Modified: Fri, 10 Jan 2025 00:07:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:60dc2978fca4afcd009aebe5d758e91f57121bfdafca39bf4e5d5f1dceb090aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f2f4d87f5732bf8bf40914714cd9e4e44a3c2f000b0daf74c24652f9555055`

```dockerfile
```

-	Layers:
	-	`sha256:4b3c50b38f4a51b92b60b2481ead3266c60f4181ca429803441d36b6fca5c1e7`  
		Last Modified: Fri, 10 Jan 2025 00:07:39 GMT  
		Size: 30.4 KB (30370 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ae3448033f7ebded4859f93376f9ffd669bd1859b704198018cc22080a480c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149770315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f713d68419b41e3b5580d43c826b335c745b528944ff9b2ed21f9d9b60c0172`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 18:52:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENV DOCKER_VERSION=27.5.0-rc.2
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-amd64'; 			sha256='32ed111e941e385c2fb8261eba06a4056915718fd606f8278834ac1931d261a2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v6'; 			sha256='744352489292ab1439e4b4facfd49f81cbe25e71e205908bd9ec44618759739c'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm-v7'; 			sha256='5a83e1663b595147ac0225d876fc77e3b441e62dac7a59523ba7003eb6733b8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-arm64'; 			sha256='138b587399b27bb61945a36d67866177b85dea1155101a2be63c7ab715f18a2e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-ppc64le'; 			sha256='b9eb337b16a75ad45ff846134d34599169bc6dfdb168fb51303fc6b08ed9f31e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-riscv64'; 			sha256='de8151fe6ced7118f2d680e1d1e7c5cb00496ca0e8b0f8b261450c6636d86978'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.linux-s390x'; 			sha256='422a9a0250d52dfdd6b78c8152fbf9df41993be4c7add93438c22122ff6c7da8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-x86_64'; 			sha256='e746a42f33113ca1057a72adff5f07d584b38c94dd7cc8368f6a30c276367710'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv6'; 			sha256='7a527b3c21d2e9f1f98cef3b37ad2fcb84f410dfcd67916e6fad78123155d216'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-armv7'; 			sha256='556710d309f248fffbfab835c1142e32ea9dd0b1ccfbdbeea2624db0f35c68a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-aarch64'; 			sha256='c5b795b304410d46a754ecacfee36bf1f341e3bcd562a882525115e09ed90d6c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-ppc64le'; 			sha256='4eb2cac95680923c50bd1b1248e460cafe99ebaa063e394dd5178bc4065e0efa'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-riscv64'; 			sha256='d007f7dd93ea364d1e341e53308691f61cebb86a45b63d002157c22cba80510d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-linux-s390x'; 			sha256='b91db23ea592c81162bb92b042873569cbe1e381400ad45447521cfa984bc184'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 08 Jan 2025 18:52:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Jan 2025 18:52:25 GMT
CMD ["sh"]
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.5.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.5.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.5.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.5.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
VOLUME [/var/lib/docker]
# Wed, 08 Jan 2025 18:52:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 08 Jan 2025 18:52:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 08 Jan 2025 18:52:25 GMT
CMD []
# Wed, 08 Jan 2025 18:52:25 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.5.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.5.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 08 Jan 2025 18:52:25 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 08 Jan 2025 18:52:25 GMT
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
	-	`sha256:8bcfe8386e2237fec90daf19cd8ba491dfd16e22403ea006d78c74d9e304e7da`  
		Last Modified: Thu, 09 Jan 2025 22:29:24 GMT  
		Size: 17.8 MB (17795789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a1a11b1c0f7f2eec8de0dee32306eb07511123c3079e8d30e5d2c55291cf73`  
		Last Modified: Thu, 09 Jan 2025 22:29:24 GMT  
		Size: 17.1 MB (17106442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41348e1c5583cceaf0d743a287b5829751e2de935eed8a50c782219d9792989c`  
		Last Modified: Thu, 09 Jan 2025 22:29:24 GMT  
		Size: 17.7 MB (17653974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1e54ea85aba2ead18cf01620a297d57612c95088894b00881fffda27f1e5ea`  
		Last Modified: Thu, 09 Jan 2025 22:29:24 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14bbbf7fcfe04dd9d925b93b69abdc72380976ef81bbfd2dfc042e3f75b86c2`  
		Last Modified: Thu, 09 Jan 2025 22:29:25 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e82aac5329a578313454cdc01cbf748ca6cf66d7c8596e771bd64e8b648f3b1`  
		Last Modified: Thu, 09 Jan 2025 22:29:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6989ea30ef1f8d13bbee39dbf73bb925d97a037ccd7fd52b6efa480590267ee`  
		Last Modified: Thu, 09 Jan 2025 23:09:34 GMT  
		Size: 7.0 MB (6981954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19baf392355c41859c2ea9defa3cca7edb7106c24b9aa7e3c6e47d0e1beafd93`  
		Last Modified: Thu, 09 Jan 2025 23:09:34 GMT  
		Size: 97.8 KB (97784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d766edf423dba07f8abe4ebae68a21afdcd40644025eb253f01e8990104fc3c4`  
		Last Modified: Thu, 09 Jan 2025 23:09:34 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f0f775a78c61386b86b7db674eacab169f3d0c460ad6eea80e7924f6757fb`  
		Last Modified: Thu, 09 Jan 2025 23:09:36 GMT  
		Size: 53.9 MB (53890237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03feccd66769539e0ee9c446c4be714a3d7b7e28f14967e98e2e6800805c98c`  
		Last Modified: Thu, 09 Jan 2025 23:09:35 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6079c2bf379cd1e440431c005bbf629768556701be8a449e7c983f95a46fbe`  
		Last Modified: Thu, 09 Jan 2025 23:09:35 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f244414875f068f88aa8ee21ca58ca217bb7ed60180b165036ad66e3e619b66d`  
		Last Modified: Fri, 10 Jan 2025 00:07:13 GMT  
		Size: 1.0 MB (1014204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47458284a176d65c94fa0c6a5d4548f5974c840364a61d0b47d869edcbd17af`  
		Last Modified: Fri, 10 Jan 2025 00:07:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb341e2d0ff95195c363395b130f91e5440cdaf84911db6a2414210d6c55811`  
		Last Modified: Fri, 10 Jan 2025 00:07:12 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d358ab7779c12764a86ce1ee06d04e00edf47cfc6154051cf551eceae0ed779a`  
		Last Modified: Fri, 10 Jan 2025 00:07:13 GMT  
		Size: 23.2 MB (23155144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe779533bad081745f99dea1aec9e9cd3c4a400c9e131a8678a8d070e4a96c5`  
		Last Modified: Fri, 10 Jan 2025 00:07:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9ecf486813a1cf9dfb96279b1dda3477683c442640226b91fe38d8cd2d7b93f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d98dc2cf654103a3a8791fb7c160ad8c8d85bf8b3abdec4e567061b6082696d`

```dockerfile
```

-	Layers:
	-	`sha256:3b3f687741034b3314e20933cb85e746fadce825afe76baa6a158ff1fd1cf121`  
		Last Modified: Fri, 10 Jan 2025 00:07:11 GMT  
		Size: 30.5 KB (30527 bytes)  
		MIME: application/vnd.in-toto+json

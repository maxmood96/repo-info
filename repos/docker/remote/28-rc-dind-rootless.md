## `docker:28-rc-dind-rootless`

```console
$ docker pull docker@sha256:cd65f57a2a9228050716da67664b9842d8132fa6125c72df08616d7c2bc3e9c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:19019697bc5f4c4e547c13627c5ad66f6e314316433e6dc348823fc3579323a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (162042601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278a81d3be2eaa4411f330a9b682ccaa9773d85a2463908bea1ad6a51e87fffd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 23:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 23:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 23:04:25 GMT
CMD ["sh"]
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:04:25 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 23:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 23:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 23:04:25 GMT
CMD []
# Mon, 19 May 2025 23:04:25 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 19 May 2025 23:04:25 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 19 May 2025 23:04:25 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7b23c3b4999912ad99167b75cc8dc84d6ca6af20c11f1f68c40644b6690bf3`  
		Last Modified: Mon, 19 May 2025 23:46:18 GMT  
		Size: 8.1 MB (8062892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0134daf873359f252332f98eb9753da24890eee7ba1084aa60d0a5203e1abb`  
		Last Modified: Mon, 19 May 2025 23:46:18 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619c23a238f410bba3e4c223afd338c6a60fd1997c977eec5049bb6f037a5145`  
		Last Modified: Mon, 19 May 2025 23:46:22 GMT  
		Size: 20.1 MB (20090869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3d0fe20c87f58631c1ea94a880c620b880ba4afb42f376ccae2e18931e676e`  
		Last Modified: Mon, 19 May 2025 23:46:23 GMT  
		Size: 21.5 MB (21456664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b347a21e6a38a1b647276b86120d9c94c016ef0ac9f8fa3857cda0d9499bd2a`  
		Last Modified: Mon, 19 May 2025 23:46:24 GMT  
		Size: 21.2 MB (21208008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12d7a5c6c17f2211982824b58acd0dec57d153bbf90e1ae9857dbbe63dd877a`  
		Last Modified: Mon, 19 May 2025 23:46:19 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36e172d5fe9de7fe16d3e9911f481c4ecca66d9bf764c0152e5a739c614bdee`  
		Last Modified: Mon, 19 May 2025 23:46:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938669ea78e2b7b1876ba878170a1c104b177adeb87ce15465c4a8a16a6b3eb`  
		Last Modified: Mon, 19 May 2025 23:46:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfcc4ff0b10eb417f46461e67c705582d8346246d06ec6dde6ecdd168457fc8`  
		Last Modified: Tue, 20 May 2025 00:08:27 GMT  
		Size: 6.7 MB (6732959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84156838244ac5d9ba8a2b619688062231d9362e45e3b2c9aac23cfa3e0fc957`  
		Last Modified: Tue, 20 May 2025 00:08:26 GMT  
		Size: 90.3 KB (90337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79ddd6efca01b89700f40f62e357fc5ca4463318f64221cec7f4fbed74d57e`  
		Last Modified: Tue, 20 May 2025 00:08:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87458349e2b2d45f36327aa26ff2efeb40bafd50e21a18755c4b0d1353274deb`  
		Last Modified: Tue, 20 May 2025 00:08:47 GMT  
		Size: 62.2 MB (62176598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0094de59e9d9a613fd9313919a8ec45958fef8a2974f06b9487e62b29278db`  
		Last Modified: Tue, 20 May 2025 00:08:26 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2db2c92a50ecfac3a5b59f41ea7050ea7773e264f92ecb770ef4e3cfac8695`  
		Last Modified: Tue, 20 May 2025 00:08:26 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8f782604ec4f1a3dc900619f2f8338743fbf482dc47f7598ccd30c023b9b9`  
		Last Modified: Tue, 20 May 2025 01:08:23 GMT  
		Size: 986.6 KB (986577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c928adbb70316b9f82cb0241c0aa3648db2e650af1290db8f132970f47b3cb00`  
		Last Modified: Tue, 20 May 2025 01:08:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c3868174a826df252dfb2cea82f79d93a1d85d3baebe3df234837661837e84`  
		Last Modified: Tue, 20 May 2025 01:08:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb25eec1f83e03f8e70179c7edcfd1399b91751b61bad5916056a6db0af7c523`  
		Last Modified: Tue, 20 May 2025 01:08:27 GMT  
		Size: 17.6 MB (17585960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae74566b4a9cf5cd2b7a89e64cbac37fda69768bfe3fd7cba944756c0ffafb3`  
		Last Modified: Tue, 20 May 2025 01:08:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e7ffcbc9f774b735cc931365e0bfcf9d96439c20d8ba33ddab96c0adbc6a0974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32199dd7f16cd01665551c3c54376df77241a007e89e5a3c21c209f92193452`

```dockerfile
```

-	Layers:
	-	`sha256:ece742f85e6f4f7e0be3034d65a0a4c0cd572ad942e3041145668023e404e891`  
		Last Modified: Tue, 20 May 2025 02:08:32 GMT  
		Size: 30.2 KB (30204 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5e0b2160377605278cf294da9b92e92338b9899ab36c3ec9d01ec1897eb41fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153357167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26d9b68bf56dd75fa18e7c32d6f541693aee994524882b774db10aa2cd24253`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 23:04:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-x86_64'; 			sha256='8c410e789d3fa688201170a8efb52048ee0dcb0d4cde44ce92a1bb6949f49fcb'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv6'; 			sha256='4726dc002180e66122087c4b48bc58c78a7cb97c92811ff2100296c73a426222'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-armv7'; 			sha256='583299ca517b1d32cd9739b58e747770ce0e8a38cf72818d023fa5d6fb973098'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-aarch64'; 			sha256='a1ad63fe3f1feffb096df472bcd793e9635907a51e5861a0e0bf78b0c4fefa18'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-ppc64le'; 			sha256='7c208fb561bd5a7f79d16774b0b8f5c9da12f6dbe71601a8a40e4664da9ab822'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-riscv64'; 			sha256='c6de2c0d930ec37a4465ecb786aa59153fac518acbec37b5f92c23760fcb20a9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-linux-s390x'; 			sha256='c06364ce6bcd14c2b8c7c595789249d2c041f0b79ff50f59356471f7fd938611'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 19 May 2025 23:04:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 May 2025 23:04:25 GMT
CMD ["sh"]
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 19 May 2025 23:04:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 May 2025 23:04:25 GMT
VOLUME [/var/lib/docker]
# Mon, 19 May 2025 23:04:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 19 May 2025 23:04:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 19 May 2025 23:04:25 GMT
CMD []
# Mon, 19 May 2025 23:04:25 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 19 May 2025 23:04:25 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 19 May 2025 23:04:25 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 19 May 2025 23:04:25 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fffdd893f2edce36ae9ef8552b4908e678780ed400d81510a7672b934b2c9b`  
		Last Modified: Mon, 19 May 2025 23:45:49 GMT  
		Size: 8.1 MB (8077199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d86e9e1048e11c509f223efe8388ce6b460fb5a34e23a02d017ec34b2c5bebd`  
		Last Modified: Mon, 19 May 2025 23:45:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a880d1d44d4371534ca4b28c80eec1fd2004e1abbfc670ae3454922cfb9ce6`  
		Last Modified: Mon, 19 May 2025 23:45:52 GMT  
		Size: 18.9 MB (18911008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270be18cc17ab6d5b737ac3d5414e12f1f36d49025b5e6e7e87b8b1c0d261551`  
		Last Modified: Mon, 19 May 2025 23:45:52 GMT  
		Size: 19.7 MB (19692500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c124b553cb1d277688778d90650228589fbae1a123ea4159b3e86be45dbd881c`  
		Last Modified: Mon, 19 May 2025 23:45:53 GMT  
		Size: 19.4 MB (19433951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a913832b1a4edd4b816f250c3430cfd8ebc5fdcc341328eda47ff78a9c6750d2`  
		Last Modified: Mon, 19 May 2025 23:45:50 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53491eeeb37a9988871b3fa80e54941282c1c3b29ca31a668b15ec926957a444`  
		Last Modified: Mon, 19 May 2025 23:45:52 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529aaaf3143411c3f67529a626ce1cbe3874db6ca52e1a9bb2edfdffb8f03fe1`  
		Last Modified: Mon, 19 May 2025 23:45:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dacc6c592c6ce994f92c9fbda287a976331b4459d792a48aa6ef42f7194ab5e`  
		Last Modified: Tue, 20 May 2025 00:25:45 GMT  
		Size: 7.0 MB (6978939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d599fe75955d3a82f5da99b9a7c6f44d2062487356ad413a07b24af6b0df7e8a`  
		Last Modified: Tue, 20 May 2025 00:25:44 GMT  
		Size: 99.4 KB (99393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58537c4f289996a00c8a08df3bd5295a1accf017e4bcaeaf2a82137b554e1c`  
		Last Modified: Tue, 20 May 2025 00:25:45 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4c068dbe9848df0bad10c66e732b226e79d3a333116984333aa219ad4724aa`  
		Last Modified: Tue, 20 May 2025 00:26:04 GMT  
		Size: 57.1 MB (57131286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3efae52d7fa73e6a6458e303a097bb8f510b492e4abc864a4241b093d1418e`  
		Last Modified: Tue, 20 May 2025 00:25:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce8ebd1b13c7930b48dcf7b2f3b284f5ecabf6ecff80af66cf12763845950a7`  
		Last Modified: Tue, 20 May 2025 00:25:45 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56f1360f12ec7ac9ead45cd19164b62bb7553c0942a27e15d2adebead8c2902`  
		Last Modified: Tue, 20 May 2025 01:08:03 GMT  
		Size: 1.0 MB (1014225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf33b27ce317b7c7acab4ddbd41e3b3445e037c225e225591b639f649d920c9`  
		Last Modified: Tue, 20 May 2025 01:08:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2f0486a36c93fec6d46c6fe6765014a7cee168786186ad10927f9b5f147c0d`  
		Last Modified: Tue, 20 May 2025 01:08:05 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc26805cc3b6824066ee570e5ef689d755092ee677224777f0a409e327f4d22`  
		Last Modified: Tue, 20 May 2025 01:08:08 GMT  
		Size: 18.0 MB (18016147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d78aa76fea28ba673556f34f3b0e8c3d5da5d49293fa6a57e22888422cc343f`  
		Last Modified: Tue, 20 May 2025 01:08:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d267e8d6030632a4ff7b18b0de592022322f80a55e9b87d2167c8336038fd3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026781df605b803ca0774bcd5a05a6acb3e165d454a21246fcebe9b30ec7f346`

```dockerfile
```

-	Layers:
	-	`sha256:a0b3480f2ee7d7ee0bf1c9af4f108e9adb8679d71cfe47fc029c110334dcd12a`  
		Last Modified: Tue, 20 May 2025 02:08:34 GMT  
		Size: 30.4 KB (30361 bytes)  
		MIME: application/vnd.in-toto+json

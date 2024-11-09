## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:73f50b3bce5075a058930176a323afb6a41b3f952e4067b6e1d38a08bc465f2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:16eb0169385e144bec28f48ccb1f3a1ea1aff628c129b8581ebb01043cf8927c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157010574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cbd54f378605ab315c49809ccee9a12dc07756245781d20d390cd990277203`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-x86_64'; 			sha256='fbb4853d3f2148b0f2f0916f8971c9e500784e4e4949324934fc0b7dc2ed5016'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv6'; 			sha256='7116c73bd22504ff61e5e25f3ea6638a7b2a5d126764fccdec4fd7623cf17963'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv7'; 			sha256='944402b85b5eb8492ebbe2e4dcbf962adcaaa16b0ed66b51abaf2ac3e3809b1b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-aarch64'; 			sha256='8fed7b79b8bd1cb0624142f7d723c3cc67ba747c77ed69abbdefdc77a6d416d1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-ppc64le'; 			sha256='9a5d9fd85e852a9c3c9137ea8ea80d66f0fe349d34b3e329255d98cd960c331e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-riscv64'; 			sha256='eda617db72d24fe79be98e2273e1fb433943a18479cedc86601963f75666304f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-s390x'; 			sha256='9476a64e9605df956e3e33b09acfdaed2d4a2c71da5b4a09899a9b7d428263a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d54a3aade6eff1cdd9e78b1df495a4f08ba7c73c29cb42cd4fecd9edef9505`  
		Last Modified: Sat, 09 Nov 2024 02:00:20 GMT  
		Size: 7.9 MB (7889966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75c42edf92c01017a85b0a5bf6c7e49d064bcdca350a7764fa1b46bb824727f`  
		Last Modified: Sat, 09 Nov 2024 02:00:20 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3728d9cc2aff530ad7f9c758c88f82e05264b8b1a1bfa7dd474e330474b5af`  
		Last Modified: Sat, 09 Nov 2024 02:00:20 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9116f7ee1dc0303eeb4e7c6fda422d38643498a9c419fd0373ed67478e9e8c`  
		Last Modified: Sat, 09 Nov 2024 02:00:20 GMT  
		Size: 18.6 MB (18566632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e123e80dfb98e5bd393dc8d0c0489f62d2c98ceb4df73bb4c6b8eeada815d51c`  
		Last Modified: Sat, 09 Nov 2024 02:00:21 GMT  
		Size: 19.1 MB (19117166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d75d0d064b19490ccd80d55683d5de424ebb3b45702111383769d5b38d8c5d2`  
		Last Modified: Sat, 09 Nov 2024 02:00:21 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65f629885e432ecda7562cd694b7a224d5c5d7a8c8fae3da7f2785b5bee1736`  
		Last Modified: Sat, 09 Nov 2024 02:00:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdf08f2c92e8a5bdeb90a92412311559f73b841ea1d4f5517ce23a45800f03b`  
		Last Modified: Sat, 09 Nov 2024 02:00:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba65c0cc3aa726a7a2e7eba9f189cd59558607098f91063070c566f45f5d9c1`  
		Last Modified: Sat, 09 Nov 2024 02:50:40 GMT  
		Size: 9.1 MB (9067247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4ddff99afe41e0535153b0047dd5f346733ad18efbc0f06724df63c8d3aa5`  
		Last Modified: Sat, 09 Nov 2024 02:50:40 GMT  
		Size: 89.2 KB (89241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f214c9427515de680d354627710e3db61bb89a0e43c48c3b0cdab768ec87157`  
		Last Modified: Sat, 09 Nov 2024 02:50:40 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ebe1a821ec273f438500601a7ef6f691c3a49a94f0fbdd9c25486c5cd07f69`  
		Last Modified: Sat, 09 Nov 2024 02:50:41 GMT  
		Size: 57.8 MB (57798962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284d5391ba58c6415cd63a454f9002ec0564b5cb5b8899313a4c08a2f6adabcb`  
		Last Modified: Sat, 09 Nov 2024 02:50:41 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7cadaa1f799d36edb5a0d0299a73e9c4736952e6568a2a07785d4966957d7a`  
		Last Modified: Sat, 09 Nov 2024 02:50:41 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8aa3ed8fbb0d7995a537a2b9100e7f0756cb0761bfbdade78e276a2d776c4d`  
		Last Modified: Sat, 09 Nov 2024 03:48:28 GMT  
		Size: 981.6 KB (981577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278ca26fd0f1ece64e6252bef08f8036e0d0e2cb7229ddcb723055835d0a1164`  
		Last Modified: Sat, 09 Nov 2024 03:48:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401943f23364e4c7af4c3b2158f3fbf5cfb590dfb9374f15ae2408eb14220d71`  
		Last Modified: Sat, 09 Nov 2024 03:48:27 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2734de92198f7e9b014e69dcc2298d9f5c1c8f048c633000857d83aa6bcbac`  
		Last Modified: Sat, 09 Nov 2024 03:48:28 GMT  
		Size: 21.3 MB (21303261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2bf69b9252e6c9cc75e21c14ad36f2d963d0c85c992f7919bd2f26fb128df5`  
		Last Modified: Sat, 09 Nov 2024 03:48:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b7bc0e0fa5edf2d57cef13984c7786bbe022c37f68705eae17bc53c173dbc91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a8d3a7f94090b32991d5fc85ff5d68fbb3702e6d5ad64dea6ff59f42ebc7ea`

```dockerfile
```

-	Layers:
	-	`sha256:7f2cd77ba26c04e81840ff32d27dc375e62ea96cfcabc4f1c7e4040d65b3108e`  
		Last Modified: Sat, 09 Nov 2024 03:48:27 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c440a28534d6544b5558dd0704056b6fd9e0f0c5a62be916c49d3cd1f567cb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151567593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d526e74b8806132257687769680ea4729adb42efab11e5f5f4a1eade77d5e1a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169407c7aadb421feb504617914f9976cb307e40ab12702a1d99169d2188880`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 8.0 MB (7997681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa20d0c1f4ec67c0bacd2cbd4b10590ed09e1e49e9aa3acac8e19f790bd2cd1`  
		Last Modified: Tue, 05 Nov 2024 20:23:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250351a83d4a46e4448b8c0dbdd9b9f1668372f21e5bb1baeda334068f29cce2`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666875d2df5ea2a2d4c64c2f12728b7f5157e64a07bcb2961c53a759eaf45d8`  
		Last Modified: Tue, 05 Nov 2024 20:23:50 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e8b50fcfaec79d0b93557893b714c17d53b1a37ee5f4979b9b8ede23e02b8`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 17.5 MB (17492822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d538de72325492065935bd3f0f9abfe70edde623d75026efe857bb7d12646d`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a8752f775fe2c4811358f822e059a13b1b5dd4ef693c3b7ffc7311064ae53`  
		Last Modified: Tue, 05 Nov 2024 20:23:51 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab7b86a6c3c38cb7821fb5778aba190bb4715c14feb9b5011a7b802888e877`  
		Last Modified: Tue, 05 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4427a880ed59f6adfa79fd5dc3e980bef68e77b66cf3d76aba5adc9d52f8cb6`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9537b116b95a7d7a0e548f885d7bcd52817a801a6684fa9e80e48f486b021`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 98.7 KB (98656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cc4cd768d96aa665871b3eafb83119cca3156723e3b4f3639dbb64db18872b`  
		Last Modified: Tue, 05 Nov 2024 21:10:18 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c963033ddf346f88bd55f8e5b5240e35a97e150838b8f69c271802fe9d6fea01`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 53.4 MB (53428160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a949f34dacc6cae826762ebd59846f9d3de501d2bd2a7326443ee034fde96f4`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca971b7fb5c65856157d8243666a4d27fdd3b84e63137a705178623b2db71c9c`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1c6209f8ece05c0310870aae2e391cf1c0f536677211222057496b38634016`  
		Last Modified: Tue, 05 Nov 2024 21:47:36 GMT  
		Size: 1.0 MB (1023839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ed16a9f9298720d2949a1bedaa297a4509064eb0a71967f5fc7a326c832158`  
		Last Modified: Tue, 05 Nov 2024 21:47:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b228cbef45601bbc062075754c4462e987a42cce08a01c6bbf26d8cee7adcf0b`  
		Last Modified: Tue, 05 Nov 2024 21:47:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142e9cff7aec27e6a409a8483598d0eca5f28d44a830503ac9239ca69d12eb76`  
		Last Modified: Tue, 05 Nov 2024 21:47:37 GMT  
		Size: 23.2 MB (23155434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9ed5aee51877fa17b27761b121944116006477bc8cc5ee5376ca8494b1432e`  
		Last Modified: Tue, 05 Nov 2024 21:47:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:df316d394f2282f93ca50a5b82ccdceb292c9ee96ddde7cc47e0e02210e5a700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaef0858e11a6f981140de9773b1b1d92ca183ae0b20f88dc053e533dc3413f5`

```dockerfile
```

-	Layers:
	-	`sha256:3e2b1bb9f6b7e9935d65d654d0d0f03dae4afb41cdab8cf1017b4f388f800f33`  
		Last Modified: Tue, 05 Nov 2024 21:47:34 GMT  
		Size: 30.8 KB (30823 bytes)  
		MIME: application/vnd.in-toto+json

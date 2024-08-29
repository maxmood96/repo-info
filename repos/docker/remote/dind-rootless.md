## `docker:dind-rootless`

```console
$ docker pull docker@sha256:d4b65d97143df48e3d62552767c761acd1caeef690e2e477f7afd49936e7010a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d15ad34856867266df70f76dade85460fed6b843d61b7407e48c471f6c0a2001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152544902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9beb99a89c140e01826af249681941858ae9a3f0f4ceef0a8deeeefae295cac2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.2.0
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 27 Aug 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
CMD ["sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
VOLUME [/var/lib/docker]
# Tue, 27 Aug 2024 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 27 Aug 2024 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
CMD []
# Tue, 27 Aug 2024 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Aug 2024 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafdcf73007468fe9a76f67bbbac5511c64f32be2b4eae1c84f9e17662c3c245`  
		Last Modified: Wed, 28 Aug 2024 20:55:38 GMT  
		Size: 7.9 MB (7872542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86396d290d332dcc402c9e2a59f4a5b85b6d962cc77ce2737413ec23958930f`  
		Last Modified: Wed, 28 Aug 2024 20:55:38 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46683f53523bc7f8c2866d515c5bbefda1ac578307b96a5d2483f54dcc27eef`  
		Last Modified: Wed, 28 Aug 2024 20:55:38 GMT  
		Size: 18.3 MB (18322538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94b3f53e3ee04d5e973346678f4c7b947a1fbd7494bd0e5944736a9d747b2f7`  
		Last Modified: Wed, 28 Aug 2024 20:55:38 GMT  
		Size: 18.4 MB (18404795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1b4b8e0ce94d538a2b1f3798ce7d4e8571cf9f380e1c089aa73242bb14131d`  
		Last Modified: Wed, 28 Aug 2024 20:55:39 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb908945666f2093de2e51e75c5046285931570429ed2bba440bea122f0488a9`  
		Last Modified: Wed, 28 Aug 2024 20:55:39 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ed2b6301eefca20d3f6e0a1e5d3047afddaa71c53de0edd93d8e52cf080540`  
		Last Modified: Wed, 28 Aug 2024 20:55:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45a78d29be2795c26b1d7f5d2b6077152f60ab369abe7e234bc21aa7edc8a6`  
		Last Modified: Wed, 28 Aug 2024 20:55:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5999d1eeaaaa2234abe46f948bb0ebe9312f43a2105d221e444ce83d4f3cd61d`  
		Last Modified: Wed, 28 Aug 2024 21:48:55 GMT  
		Size: 6.7 MB (6657782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e81507025f5194d6dfed1a0639913352223b58af99a369dd3ad14500a9d48c7`  
		Last Modified: Wed, 28 Aug 2024 21:48:55 GMT  
		Size: 89.2 KB (89212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6529ac1dc972936d686ca9f28b883acc1aea3c07842876e5092bb988181529`  
		Last Modified: Wed, 28 Aug 2024 21:48:55 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4361b74540df0300612edc589ede8fcbd9401621040e525dac987ac89e729086`  
		Last Modified: Wed, 28 Aug 2024 21:48:56 GMT  
		Size: 56.8 MB (56779820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bfdeabc852670ac6c9f0529df1fe1d3b4474c9a6af4c88b41cfd93bebceff7`  
		Last Modified: Wed, 28 Aug 2024 21:48:56 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903c78ead876cb384be6034b1b0dec8e7077a83a82eb603e405e20c5b816d4bc`  
		Last Modified: Wed, 28 Aug 2024 21:48:56 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5284fcc545f2d4a2f595d05598892e85f9c7e8a8242a712fff1482041b0ae2b`  
		Last Modified: Wed, 28 Aug 2024 22:49:08 GMT  
		Size: 981.0 KB (980988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65db6b87f8895c62f76892d0fbf4d071a659e0d745bd306fea060f9a2c3d1d8`  
		Last Modified: Wed, 28 Aug 2024 22:49:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c38b0d832f4caa63b21e54e778d9abaa9bcaa029c7059e34eac7b2d996f28c`  
		Last Modified: Wed, 28 Aug 2024 22:49:07 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bb45367943951752b5d81947bb08588f9f1d20a82236ba3c9f50cbedf0bbe2`  
		Last Modified: Wed, 28 Aug 2024 22:49:08 GMT  
		Size: 21.0 MB (20979751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4002f30159a34d4d7900b53969053725806d68bb15749a7dca8dae26e7dbbc1`  
		Last Modified: Wed, 28 Aug 2024 22:49:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:63c526e78ef766623d42be9368e23ddd61a5fed1e3f804cb90295d561497a8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012bed201565f5d5b9df2b38cf0e8ac344d910fcaee72e4dbb23d1b0b245ae06`

```dockerfile
```

-	Layers:
	-	`sha256:59669eea1f0a249b72c1bd0156b987ef8fc059bc679e94d0545744bcf98736a6`  
		Last Modified: Wed, 28 Aug 2024 22:49:07 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e3fbe21c151e4271d73fa228238bc61f32f660c550aa54e3527a460c27bac3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146696891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9187071f9b3d29959b0bf9a17b644db2d13e09317b504659a69884c6717ac1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.2.0
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 27 Aug 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
CMD ["sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
VOLUME [/var/lib/docker]
# Tue, 27 Aug 2024 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 27 Aug 2024 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 27 Aug 2024 23:04:15 GMT
CMD []
# Tue, 27 Aug 2024 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Aug 2024 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Aug 2024 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7ebf14e366b1f6bb3a236c7afda2fa7f972ec82687bdfb1faa44ff909b3c7`  
		Last Modified: Wed, 28 Aug 2024 20:55:20 GMT  
		Size: 8.0 MB (7981883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70774fd8129e715db6bdde0a5fa9a8126035d57497c7abbf3918ff783e3839b9`  
		Last Modified: Wed, 28 Aug 2024 20:55:16 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75bde5fae086c68bd31219b257fd17de34da8ae7534ba873f2893aecb170265`  
		Last Modified: Wed, 28 Aug 2024 20:55:17 GMT  
		Size: 17.3 MB (17266013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d280a0d728e728847e4bf2aea17b91f3d0b0341f060af4931e99f3701dd251a3`  
		Last Modified: Wed, 28 Aug 2024 20:55:17 GMT  
		Size: 16.8 MB (16772961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91e7e06e5fa6595fc74a6b371d01d11c33d00755afee8c9e5526b26db04bdca`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee3d5382660f041e5d6a4e7e5eed70a981eb51d8f65e980dc17b77257f5d1d`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e7d5e3ae6089103a06ae9421106617e42616bccfb18af4a99a047a339b59cf`  
		Last Modified: Wed, 28 Aug 2024 20:55:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6843b239ba63d521157d7d1a46d9346bf6fd58eec87be84f52f99b62a8fb2d47`  
		Last Modified: Wed, 28 Aug 2024 20:55:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c047d9d5cf44cdaa49f139b96bfad8456b4544e7f8dac65b22512b54b5c27785`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 7.0 MB (7034976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8566c5e148875679770fa70b5d8461643fe4f3e523cc4c23fd5048921979993`  
		Last Modified: Wed, 28 Aug 2024 21:48:45 GMT  
		Size: 98.7 KB (98665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e81cd465f9ee02216b68ffcd601579cf2b466ec9cfe9eab7d1848715d5efb6`  
		Last Modified: Wed, 28 Aug 2024 21:48:45 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfc280f1208cfd219d0f5c9ce8a5485366216b0690ca15eac47242a174ec3ec`  
		Last Modified: Wed, 28 Aug 2024 21:48:47 GMT  
		Size: 52.4 MB (52400296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f850c0ae6138cdad5371b2e2f80f46619b8f1e83fd23719f35d80c4e68fd4`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494ac230758233bbef46064dc8f7048fff0763039a7c97d01acd30d1e1a6b16`  
		Last Modified: Wed, 28 Aug 2024 21:48:46 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61d4b5e595f4a9dcd2d5b73dd64893b48b8b5c325e6c2a77f7d87c3bf774b63`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 1.0 MB (1023147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4970a08325e433d212e5137f22b0c5f9ea602fe6d34c30ff0af92e85d826d457`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f824c9ac49392520b799e62abf06ca24190d5c747d6a8665d62f17c60adaf174`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5468a19c79fccedbe38a88979c4a5da92b1a73c727a9b3fc58e11bbabd3e9256`  
		Last Modified: Wed, 28 Aug 2024 22:48:38 GMT  
		Size: 22.8 MB (22835883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49084cd44b920e2654ce7a8f2bace247f0acd7ddfc481e9365b9c39c01dfe57`  
		Last Modified: Wed, 28 Aug 2024 22:48:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b7cefe17c5a87b42bf6cfcec3b08ade5272c29f153f8fbcb770707bc1c20ccb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6630734a56a43074699439ce4c6d79ac0ec2972110823e0d46a936ece911b64f`

```dockerfile
```

-	Layers:
	-	`sha256:c50ad41cecb6f30ac11d08ace289d54c454da27e48229ef60c118eee48306b88`  
		Last Modified: Wed, 28 Aug 2024 22:48:37 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

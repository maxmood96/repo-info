## `docker:dind-rootless`

```console
$ docker pull docker@sha256:902c9401a3c5cbc96d1aca05e30f7371503a1adbae2275b21dca9ab1b53c0e8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e764fba23c68f7408452253c9ca566825eb49f723f7457b9739e0abdc0bc485a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159172172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57117dfde4a149c901988add9a9dd75f9484ade3a0cc6b987f675166d880783f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bfa185fe18c70ffc7fbb87fcac5bda6cd1a87a0199a93c5a935976d778a2ed`  
		Last Modified: Wed, 26 Feb 2025 23:26:45 GMT  
		Size: 8.1 MB (8062966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f1381044385b2725f476df58ed4d92403ca9541de0eef78287de550e51764f`  
		Last Modified: Wed, 26 Feb 2025 23:26:45 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e97ed2623950e933eb128bf578ac674d2db63dc11ee577efcec4e3dfff4470`  
		Last Modified: Wed, 26 Feb 2025 23:26:45 GMT  
		Size: 19.5 MB (19500690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26db062d70c700a0e6d3e95f27d40ef3f4b5cfa65feda4b55574ac4affb05e0`  
		Last Modified: Wed, 26 Feb 2025 23:26:45 GMT  
		Size: 21.8 MB (21829133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6788442cb8d118fbab9b36273cf40294646e85d6a8018f944cdab325299e9d41`  
		Last Modified: Wed, 26 Feb 2025 23:26:46 GMT  
		Size: 21.0 MB (20958636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9a479d2a38f7589c27b3f6c11cafdee6db7f378f226a74d782529d71dac1bf`  
		Last Modified: Wed, 26 Feb 2025 23:26:46 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdfaa5ebfd96dd86403ee1e18432f6ef66a97b53b3f276c0b1540e31432f161`  
		Last Modified: Wed, 26 Feb 2025 23:26:46 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2916b2f09977415ff684725834c8bf28e21ae894d608fa2666483626b4cebb15`  
		Last Modified: Wed, 26 Feb 2025 23:26:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df415b007716335968894f9a67285ec56d21e1fab1856cae15684dff9cd9eca0`  
		Last Modified: Thu, 27 Feb 2025 00:08:23 GMT  
		Size: 6.7 MB (6733019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3a6db14c03287ec44479ceb91eeace2a99ae09563ae6499f5884500e87739a`  
		Last Modified: Thu, 27 Feb 2025 00:08:23 GMT  
		Size: 90.3 KB (90319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edb9ca0b8ab21b6849f0c646aa929f978a650f7f41c74dca2bff2433c7e7f4e`  
		Last Modified: Thu, 27 Feb 2025 00:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bd16a408cc7e6e08316b7db9d0682c739992e8dd32189745b9cfed6cbf0f18`  
		Last Modified: Thu, 27 Feb 2025 00:08:24 GMT  
		Size: 60.2 MB (60192788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd0c4eb3cdc4ecfd68688b126f8bd89d6eb217deb291c6b08bdfdfb59b9ab85`  
		Last Modified: Thu, 27 Feb 2025 00:08:23 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a896671e16157325546fb5da4a30f1b3511a9520606745a7445f7713c04cfb1f`  
		Last Modified: Thu, 27 Feb 2025 00:08:24 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b157636673d641d922dffe448c87d26b448d3ab213ab7b36cf5af5e515280ac`  
		Last Modified: Thu, 27 Feb 2025 01:26:25 GMT  
		Size: 986.6 KB (986581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bae3933e3d6af03d1f9d4bab8ce1c8c36f244894c51bc2820423e993701de9`  
		Last Modified: Thu, 27 Feb 2025 01:26:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24f3442f52a388a0aabb6c0e9b6c683ec1720ff044876b7b3bf6564e8e1fda0`  
		Last Modified: Thu, 27 Feb 2025 01:26:25 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bb2f83c6c91a54fb16db2800723e6eaeeb138dd133c91076f8959f11f3f41b`  
		Last Modified: Thu, 27 Feb 2025 01:26:26 GMT  
		Size: 17.2 MB (17166397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f63318afc8f8a7c5627057b5ed41fa3f62f34c85e8bb24ede8ad78cb8a8c84`  
		Last Modified: Thu, 27 Feb 2025 01:26:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:219d19046ce1920ef5c842406b13c4cf26098cff3a5e9986c121f35ebc361a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085329e037c6ab705a83e83de051117439728f448ef0975a88ab4aae575b14a1`

```dockerfile
```

-	Layers:
	-	`sha256:4367bddf9603e71a949030f65c52545f77b2225e86a5b92b0ed7065e391af505`  
		Last Modified: Thu, 27 Feb 2025 01:26:25 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:41f2987d0f87935d3190bcbe3454c574c42153b867f943c6c9bfd99025543dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152706913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432414c7a530fbb36794d0c7c0fdaa59f28993b10b154724ab99682b0629868a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_VERSION=28.0.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD ["sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 26 Feb 2025 17:43:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Feb 2025 17:43:10 GMT
CMD []
# Wed, 26 Feb 2025 17:43:10 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 26 Feb 2025 17:43:10 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 26 Feb 2025 17:43:10 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645e85e6adffff3a1ef132a0c45284e30d77f1e03b73d6f6fbbd730b96030b0`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 8.1 MB (8076419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a828a8ec2d9ca9099b41a4b5d184dca94565b0d53c115e33ece505350ff8b9d`  
		Last Modified: Thu, 27 Feb 2025 00:19:33 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125a142d350ebf75ab9186985a1c97fad26b6ccd127408a89640d013b2376b91`  
		Last Modified: Thu, 27 Feb 2025 00:19:35 GMT  
		Size: 18.4 MB (18425644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a085f9cdcf8e5d11c5e69a0eed6c2999b155dd707ec91b26a2f23e39b3fc40`  
		Last Modified: Thu, 27 Feb 2025 00:19:34 GMT  
		Size: 20.0 MB (20041453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3477fc67be128d6932d6b755bfffb5c6cf38f50a5b62cff71c44c807aefeeaf`  
		Last Modified: Thu, 27 Feb 2025 00:19:35 GMT  
		Size: 19.2 MB (19222713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ec4020f9a9ce75118d83bc55456f7e65b75c8884a47208246903dcacfa2d5a`  
		Last Modified: Thu, 27 Feb 2025 00:19:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffaf949d24a15809a0ea53ece6fe4513fecda632b607059771dcebb9a27ee55a`  
		Last Modified: Thu, 27 Feb 2025 00:19:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4928eaf33fc90f08e3cfd2cb0a456e19e55a75a316c002364443ae9cc67c94`  
		Last Modified: Thu, 27 Feb 2025 00:19:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962857e6fcfdc27d09d475ff75a34e0c41bceb08c3102f2627fa142fddcc6ae9`  
		Last Modified: Thu, 27 Feb 2025 01:53:22 GMT  
		Size: 7.0 MB (6978819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7815059a55c3f6398e78aed0ebba4d528b8b03a5b18d2b684180d732dac8284b`  
		Last Modified: Thu, 27 Feb 2025 01:53:20 GMT  
		Size: 99.4 KB (99379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce3ec4fb4938d46d8f73dfae7d4ce2f327419dc01f357e0fe3de7f9a6614ff7`  
		Last Modified: Thu, 27 Feb 2025 01:53:20 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c0a5399acdf9f269a58f9b1c37634304babde20341e0534787950f2658cd89`  
		Last Modified: Thu, 27 Feb 2025 01:53:22 GMT  
		Size: 55.6 MB (55566417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee527d8ec1d04866d4999f71b353ed52cdc1ab30a57d7072861b1386f0034e3`  
		Last Modified: Thu, 27 Feb 2025 01:53:21 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33482df2e9eca1501d57c6e86ddfc51c9e47fadcde6dd716d52a8a8bdfcd4cd6`  
		Last Modified: Thu, 27 Feb 2025 01:53:21 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bda7efa1b40b738f9b27054b632e70f69bbcce62d64780e684ba3363b99beb9`  
		Last Modified: Thu, 27 Feb 2025 02:07:23 GMT  
		Size: 1.0 MB (1014201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2065cac946ad6a98d2dde47ee9d21898dc6074b104ccf944a15252705320a13`  
		Last Modified: Thu, 27 Feb 2025 02:07:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0217f6dc3d6a30e4618f0c0adca7088d88ec223bc2352c1d340751406f8969`  
		Last Modified: Thu, 27 Feb 2025 02:07:23 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da5ae988eec6a0e52e62fb4c141027c3945fd5f9a40b00dec29a4c37efbcc89`  
		Last Modified: Thu, 27 Feb 2025 02:07:24 GMT  
		Size: 19.3 MB (19279435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb59067b404955356ef6f176b4996d75e7026be7efcf735dd9c957abf130b0`  
		Last Modified: Thu, 27 Feb 2025 02:07:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e91cafeb3830da9220ba0ffc9549dab0f98f6bb7135a7b40024c0cafee7f4b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00b526396f7c2268d367f5416919469709db6f1b5b457cea7205457573245cb`

```dockerfile
```

-	Layers:
	-	`sha256:7449a06b48c3b5d1256cf228f76dde4a513def00f95185858af1dade7476bcd8`  
		Last Modified: Thu, 27 Feb 2025 02:07:22 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

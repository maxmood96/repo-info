## `docker:dind-rootless`

```console
$ docker pull docker@sha256:f36f8f41d9e38bae8c3d247446a1e31df98bd84d1ccc22d9d8d50fbe6cbafae8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:16356585ff8acaa68e6bd54dd11f6760ce507fa719fe7e00bc7db05f53c7a074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159160666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f413ddafbf744ab3b46d57ab5bda7d4b4ed64aa0ac7f3bd49a3055f8aa5c604`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc498219722db61fe7f7e06295aa8b64f7e48d19d0339176689ea591eea4ca`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 8.1 MB (8062985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c17b75175e66b76074511db7ebd5bdc56ac19ba269d30e4f58ba4812816ad4`  
		Last Modified: Sat, 22 Feb 2025 00:27:26 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987b6d8519d32209785b3840639a10aa6247ff1e290a651ebcca3d8c33e23dd2`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 19.5 MB (19492233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7677267af1ddfc39dbdf35dcdca7c20328e83a42b64595f0d5880c62e99a91f`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.8 MB (21829139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa9f5140fd1401e5edaa2de6f975bd14f0b79efbafbe0d2497ea0213ecd260`  
		Last Modified: Sat, 22 Feb 2025 00:27:27 GMT  
		Size: 21.0 MB (20958635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124bcf7a51a8a140479ebb1cfd0aea5bf38223d37b7c6ae1deb93bbb1abc0469`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083b3dfd2242fbeb7b498bb2e0d99d55c8e34cad7396573784aa86db3c69355`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b255e6bd488c8fb61ba962afb512c02077ecc7e41b50991cb3229aaa7ae94b`  
		Last Modified: Sat, 22 Feb 2025 00:27:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42458739bc4b2677f265360a10a2eacffd5133b0242dd313ba8a3dac7a116c4`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 6.7 MB (6733003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5a7650793a22cfeac45c6610fe2cd3ccd26b6795d33ee5389d66a174c05a65`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03749f129a866bd1cf2e2797db758f883cf177f3cd33ff3c60924ec811728b4f`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e1c97b1855704d1f74c39b30c2d2bbc890339752b2be542477e64d2529c32`  
		Last Modified: Sat, 22 Feb 2025 01:08:24 GMT  
		Size: 60.2 MB (60189735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e450e39e6d5b103505878dd35ff532dcdfef40450540495b6a666e7bc34e2587`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254862f49c6f0929e44b00f9635661aff98a508d2dc321d6ddc2944f60ac90bb`  
		Last Modified: Sat, 22 Feb 2025 01:08:23 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d666bba697d05e04595251efc48c7cfb46c50934eb5e8b28f9ece93bbaa12f`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 986.6 KB (986572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e9040036c95835735c8d16482226c61fd43befb113e4654d11899b4c82c24`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773fc7dad6ddd06fd1b5c0d2b81528878a1c879bcfed7b967fed225ec4346a7`  
		Last Modified: Sat, 22 Feb 2025 02:08:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0abea1fd4caba2bf7cfa1eaab27c1e81060389830353f7de69a562c0d129f3`  
		Last Modified: Sat, 22 Feb 2025 02:08:05 GMT  
		Size: 17.2 MB (17166401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e73037866943973bf1a62ff0acb7da9d1f19cc8ff52edb6c2ddf748fba1507`  
		Last Modified: Sat, 22 Feb 2025 02:08:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:788f83bf8b427ca8d5db790b94b5465dd4e729d19870cf23c0a99aa2247419e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171bb75448d4664abab1f0e5b2859c6858afa3eaf4bbe30c4ff52221ef9588a5`

```dockerfile
```

-	Layers:
	-	`sha256:681e1874c769bcd3cc3a0fe90e1caa86a29f1a172fc7caa3eb5c75bb6e9843e7`  
		Last Modified: Sat, 22 Feb 2025 02:08:03 GMT  
		Size: 30.5 KB (30451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:73776940d20eac532ae279be7c72ff89ea730517ff9dab5a659516bc00d09dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152694408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b89ed4c42e88420300229e316f2cf5c30d71c0341b7ba4039b7887870e259b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_VERSION=28.0.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_BUILDX_VERSION=0.21.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-amd64'; 			sha256='7f355525bfaf411302570b705118181b720f18071f4be3f0eaac7b2297d826e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v6'; 			sha256='f841251fd67646e8b6bb4c7e0c2c385f6a1dc7403f5ac6ee7b07c96f0815f7f3'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm-v7'; 			sha256='81d7040e90e9b69cb0378778f673e1fc2a24ef6dbd47931dc83ab6472fc5809d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-arm64'; 			sha256='42d5cee287ec7426de5252276a05f3ea565ac2d65d62d052b885a84dd54152d5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-ppc64le'; 			sha256='6a4e6a243f83d80cd46c939f327b2e14cfddd2c6690651cf48d0e208c3345b88'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-riscv64'; 			sha256='eae82aec74a420c3d1734123e6a3bc10b3a2a981aa1d538502373e31c91bf76e'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.1/buildx-v0.21.1.linux-s390x'; 			sha256='97b112b3366a471cc375e0f881d65a9a7b07f0962f308834c37f5c3fa75aad08'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.1
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64'; 			sha256='3efda1ad6caed49dedd5644cadbf7e0c9cc3d74d8844ca5237b6a43ac1ef1a46'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv6'; 			sha256='17e66154ed90d43d4c26dec4a77caeaa6f0a8337f436cc4bffecbc2fd9bcd27d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-armv7'; 			sha256='0104e689d29597352a715f7027205d7517f17f449ffe14099aa9d5d0a54f7073'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-aarch64'; 			sha256='fa0e077510c852237b0da426d0daf6853446e7760145ce7665ec401892a4d0de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-ppc64le'; 			sha256='79d874b04c972475867e2e1f69febdadc446289af32afaa0dcb99f48a25380cc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-riscv64'; 			sha256='8a51f33cb82afc6b7ce1c02b3161ce928387e96efa7b838e2f9f1fa554d68781'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-s390x'; 			sha256='bae7fd067dd05951e4c6cb66199d2e7f388b5c19856db760fe4253dfdf2a008e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD ["sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Feb 2025 06:04:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Feb 2025 06:04:43 GMT
CMD []
# Thu, 20 Feb 2025 06:04:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Feb 2025 06:04:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f26e7389ad2e79a31e03589b2c6943495faa94ce7fc6ecd800dd0c320c71e`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 8.1 MB (8076430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54483e7ea72052e991e704ef33b6d45d32f2c9886445d70ae79e50a2dd444147`  
		Last Modified: Sat, 22 Feb 2025 00:28:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747fdfb37d0ca59992c4852cab088ffb4549e3f8ef7632b252452c1c12c7989`  
		Last Modified: Sat, 22 Feb 2025 00:28:38 GMT  
		Size: 18.4 MB (18412791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84912acd39dd03fae2cffdb073ec52df5d17e2700910653a8c844d31a916a7eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 20.0 MB (20041446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49191a7f2e90fd89997d49d48799f225e27d4d811c1ab6a1a5ed18c8b5a9f94`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 19.2 MB (19222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debd3993d0af81423e3290841931e4b162ff882877ebb292b10f3dde6dc5694`  
		Last Modified: Sat, 22 Feb 2025 00:28:39 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855282ceddcfc470897f6e2cb33f2ad4742db7c00f24a0386714c91a31a090fa`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbaf9714c72f8c1c56eb53405de18b5c63f82fcfa89814a71a92c9844e1fb8b`  
		Last Modified: Sat, 22 Feb 2025 00:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1efb7aef297fc62aaca013f0102b13d4fb2bd1eb6e39c858c91c440c973f87`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 7.0 MB (6978850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d301065fd8bf09964f1efc59488efd3c692d574aae6e2460fefc3dac799912b`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 99.4 KB (99390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d33e0f749652bb606f1e92e433cb70fa6c8e7a30737050979d975e9f06a132f`  
		Last Modified: Sat, 22 Feb 2025 02:45:59 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409b11008465c3cb7523e669b4d2a064619125185de982089bf11944cf62502`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 55.6 MB (55566753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8cdce63f040e68fff768b8a75d7ebdd3f4cd4e69ed0f85ae0ad620baa9c40`  
		Last Modified: Sat, 22 Feb 2025 02:46:00 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72a632b800deed0be1fc7ec78852db28106ae059a841b87a966fed6ec7255f`  
		Last Modified: Sat, 22 Feb 2025 02:46:01 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4468cca51cdd29ea280bb7c9d7dcffc805ae2134d5d10101acabb31403f19c34`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 1.0 MB (1014200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d43f7cfe0c5e55bc699a2f0f56e6ecd213c0d84783892175a2bbabe01e1ee1`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ffc8590ff3cdff71a791e5dd600d08fee46a9a23862330e1c51e7fe2953e3c`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03647ba73f1a14d321c6973445bfedd81d7195d0c270c2a52d81c4bd00241ec`  
		Last Modified: Sat, 22 Feb 2025 03:07:18 GMT  
		Size: 19.3 MB (19279443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42024c25dd02ca9c645e8270327928627cf8b2d1ce95c86e3184f7236d8254b3`  
		Last Modified: Sat, 22 Feb 2025 03:07:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7caef0d171c210bbc06a3c6c5f181d699cdab3868ed8201206157f5ce2b26b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ce0dd66d759a7501d703e2bd782cf6c3190278388bb80297dd5fdc65839c39`

```dockerfile
```

-	Layers:
	-	`sha256:f29410d962e3aeed18fdb7f16f7e72ba75bab67d36d78eaa1f5bb9e00bee589a`  
		Last Modified: Sat, 22 Feb 2025 03:07:17 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

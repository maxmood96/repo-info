## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:fd2eaf5b4c7e7eaf36278e7abb948323ad7e639d761a07abfd452442a3c083df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

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

### `docker:28-dind-rootless` - unknown; unknown

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

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f8c1cb5a95beb1d7b5b9b55eb239c8e6faf24d0165eefcf3f043e6ed79d64afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152646612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2b5c4ab8d0497964a390eff576c882a14316c7c91817e4f79a67643a89aff9`
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
ENV DOCKER_BUILDX_VERSION=0.21.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-amd64'; 			sha256='90f154aff1b1b0010ca3e59f473a59a86b5fdf34ca1196829c622c4fbf5e92fe'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm-v6'; 			sha256='1a55ed189ee5c58b3d78459cf81d023a135a759c5ea3b7d1e2ad587cdfabac15'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm-v7'; 			sha256='542676a5aa32ecfcfcb27c56a0c8d91af42614ed5c0266e91ed0b55d90a15555'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-arm64'; 			sha256='5543113b559ca523726c8979defa24466e451dbfa6ffe42c278d22a3f76a327a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-ppc64le'; 			sha256='90c2748b59d0588cbd006e209ce8cecf202319213eba6542d01a5ce2f5c06f6e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-riscv64'; 			sha256='84148bbc57023004b186bf1ba618f987d9df51d3b588876bfc04f7a592fb9bc0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.21.0/buildx-v0.21.0.linux-s390x'; 			sha256='541b0fe136f003db4e0e5e4e3ec4ae00a647b50d398e7f63201d1ea712218132'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Feb 2025 06:04:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 20 Feb 2025 06:04:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:3a1b527e08b4ec0bd858f270bd1c73b4eb69fa1f9681172710944f5fb1108ab6`  
		Last Modified: Thu, 20 Feb 2025 23:27:39 GMT  
		Size: 8.1 MB (8076421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6666d4412f9e63506ae44900e1fd00275b8dd56bbe117245f21edb533c07d9e`  
		Last Modified: Thu, 20 Feb 2025 23:27:38 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4c9136fffa5cbeb2e6117e4694c7ea906da81198a0531aaa32145decb90eae`  
		Last Modified: Thu, 20 Feb 2025 23:27:39 GMT  
		Size: 18.4 MB (18412787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23097b21275c4fb3c71e52f2e5c3c8f7067a8cbf5b0c1b039f0ce0a91d9d59b`  
		Last Modified: Thu, 20 Feb 2025 23:27:39 GMT  
		Size: 20.0 MB (20041329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d721ea2bff14447ba40479b5a9a89bec640f22c89c1fc9c19aa7a47574de36b`  
		Last Modified: Thu, 20 Feb 2025 23:27:40 GMT  
		Size: 19.2 MB (19175074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41991d98c29dcb0ec17305e50c51cf373a30b30101d0b83a7f42b78241bb9c9b`  
		Last Modified: Thu, 20 Feb 2025 23:27:40 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a048cb704bc6ffec227160a3c0f3b515e4d6a47cf5e32800aaf51921f0b8e3`  
		Last Modified: Thu, 20 Feb 2025 23:27:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e76a992e94298f7dd06fb20218693c8af98bfeb787e13e641be48f54748de30`  
		Last Modified: Thu, 20 Feb 2025 23:27:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1af98a0761b2250294aa8e0549f273a686b0d36d5a844d569ebd214391efc4d`  
		Last Modified: Fri, 21 Feb 2025 00:26:45 GMT  
		Size: 7.0 MB (6978823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d34ed087c6d3c67acd0789cf0a9067aa7a58b8c74b093d947c2a7aa9afc2257`  
		Last Modified: Fri, 21 Feb 2025 00:26:45 GMT  
		Size: 99.4 KB (99377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adb48987cb089b5c8e32479e1e556c0ea705b5350c8181f4c3e9258d93495d3`  
		Last Modified: Fri, 21 Feb 2025 00:26:45 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee8a14e1dc617c334a84e008c5304323aeb97ec7a165786b83a8cc30e3a9249`  
		Last Modified: Fri, 21 Feb 2025 00:26:47 GMT  
		Size: 55.6 MB (55566754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b655aeae01097cc967e1dcbc3277f9e2b29baddcbfed6e2018f83418c89b6530`  
		Last Modified: Fri, 21 Feb 2025 00:26:46 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143188afd15270b0b4487b8c02ad0ba5b50b863f02d99e3c41bb43df846c157a`  
		Last Modified: Fri, 21 Feb 2025 00:26:46 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f29180dea49ae66c7bc7926ee0ccd3bef65d1fabf038525fa152b1bad745f06`  
		Last Modified: Fri, 21 Feb 2025 01:07:33 GMT  
		Size: 1.0 MB (1014193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc68779566c657f24c79525ad9dcd5c9ee3ffcf02ec3c46a5cda60769586c2f`  
		Last Modified: Fri, 21 Feb 2025 01:07:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc41d26c599adbd498428291a25daa08bec1d395f5041788675dc4b6d6e912ae`  
		Last Modified: Fri, 21 Feb 2025 01:07:33 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e9644daeeb7cd964b27d9fb1da77a254ecb25c2c25b5af0ca854b2d116ce08`  
		Last Modified: Fri, 21 Feb 2025 01:07:34 GMT  
		Size: 19.3 MB (19279435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f32d46f74022d488c81b4699aacff888d0301c2604d5665e93a34637c0742c7`  
		Last Modified: Fri, 21 Feb 2025 01:07:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:678f2f3f2fb1f6f4f47993ee1e513d82b0bf087173fa5d5ea2959690983a29c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fcb6725765cad4c7473f3e074b75927da8619de4e33f364720a8516ba1ac21`

```dockerfile
```

-	Layers:
	-	`sha256:5fe70a257c51d2754ab1d2db0953e9c3dd069fc47ea471e1c648a72885f409b3`  
		Last Modified: Fri, 21 Feb 2025 01:07:32 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json

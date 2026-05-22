## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:c3ecad06d7e5e55635b9a29b3d4b444153c12c2c8c73396794409a33b3913a18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:dc9035ef22486e1acddcc01602d5b6302dfd73b1c353df7f724bd0537ad0df63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157336930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f622391e8435f13ff5ff6528a3d376fd507daacfb4cee530a699f755e1eb34e0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:59 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:57:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:57:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:57:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:57:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:57:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:57:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:57:01 GMT
CMD ["sh"]
# Fri, 22 May 2026 00:10:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 22 May 2026 00:10:20 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 22 May 2026 00:10:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 22 May 2026 00:10:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 22 May 2026 00:10:23 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 22 May 2026 00:10:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 22 May 2026 00:10:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 May 2026 00:10:23 GMT
VOLUME [/var/lib/docker]
# Fri, 22 May 2026 00:10:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 22 May 2026 00:10:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 22 May 2026 00:10:23 GMT
CMD []
# Fri, 22 May 2026 01:10:17 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 22 May 2026 01:10:17 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 22 May 2026 01:10:17 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 22 May 2026 01:10:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 22 May 2026 01:10:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 22 May 2026 01:10:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 22 May 2026 01:10:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cf87df21c231c07f8b8d9c532474fc120946d085773fa15272382636f10b46`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 8.3 MB (8311580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54392fc3db24e998571260adc7ac1a1bc098852dfeb30150218d2174da4aa929`  
		Last Modified: Thu, 21 May 2026 22:57:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4b052546a5d5d26f7d251d92bd155e2275ee74b4c83a5748550720fa39efe1`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 19.5 MB (19549520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2deac6c9ceba582f6a7f4a7ea2910141ba0dfcf644ee930db818a78947527a`  
		Last Modified: Thu, 21 May 2026 22:57:08 GMT  
		Size: 23.0 MB (22988915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046b51e466e9d4d0fb090dd060997a0892b36578ab13f0153d1d61f53166d5c6`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 11.4 MB (11395947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff5ffb634dd2a67009edb32be895febc923676e8dc0b94f8c857528723140ee`  
		Last Modified: Thu, 21 May 2026 22:57:09 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b162b8dd068432fdb9682bbf9fc7ecbe61c2dbbb72441a22b74a6537f7fe639`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b02815b1d866ccad16190784679c75c04f712dc13f12bd8ec46cf7648796905`  
		Last Modified: Thu, 21 May 2026 22:57:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b61ce4af892f2d3ed8c9f4d176046e677d6771362b0f45c6697430c96f8c0f`  
		Last Modified: Fri, 22 May 2026 00:10:34 GMT  
		Size: 6.9 MB (6941444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cb25298c8a2c01af8c27ca6bbaf84acefe76747d23e58f00b2cda061066b86`  
		Last Modified: Fri, 22 May 2026 00:10:34 GMT  
		Size: 92.2 KB (92224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bfde0d2e54641376acebd2cf0fb9458475f1c401d697686160ff7fe8cdd34c`  
		Last Modified: Fri, 22 May 2026 00:10:34 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d714cf14f61fd37969c775d50f5c670933e3c6753eb42da150867ce04519c33`  
		Last Modified: Fri, 22 May 2026 00:10:36 GMT  
		Size: 68.7 MB (68661028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefcbbb32c3cfbb1b1fee12656b5e97ba414755750f8fba06ac142cfb9fb91b2`  
		Last Modified: Fri, 22 May 2026 00:10:35 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87a361535c9b75451c5da7eb377f1c4eb4c99c7302b9db737e26ee82b39850e`  
		Last Modified: Fri, 22 May 2026 00:10:35 GMT  
		Size: 3.3 KB (3302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e226186c9246ed254e3a0e2d9a6642de634bf9f535085c4c55c38c1f7ac3ec`  
		Last Modified: Fri, 22 May 2026 01:10:24 GMT  
		Size: 3.4 MB (3420084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a185ca63fcabed6c08e786a9ed38804aa74e2000994183ab0770899b803a26ef`  
		Last Modified: Fri, 22 May 2026 01:10:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0d010ada4a5a37e4d56ce01c83c7cb0edb8731e807cf00ec094b668d08a634`  
		Last Modified: Fri, 22 May 2026 01:10:23 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f93fabcfb676ad8d160fc4ee412cc9083aa7c2611bd0f5672ba194628f8fc9`  
		Last Modified: Fri, 22 May 2026 01:10:24 GMT  
		Size: 12.1 MB (12102499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fef4a3623462c89f71d4bd11bd6d035898f36d94cf2d414bf4a6054ff16da24`  
		Last Modified: Fri, 22 May 2026 01:10:25 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e61c099242d6b146c511fde01831727caeb9cce45e3f08103f728691bab08fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a4bf46dea288f016a49d2dc5ab9866bb1cea4a0c769559e37bef0e45a4f678`

```dockerfile
```

-	Layers:
	-	`sha256:e4eb7688478feb5b91137c8516caa926dbf1ddfd4e3dae4d1587ee26f8a9dee0`  
		Last Modified: Fri, 22 May 2026 01:10:23 GMT  
		Size: 30.5 KB (30493 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3d507ddaad8bb2f5316386a0728b020932ef433456ecf051c24a6c3f4c2aaa71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145839155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d9bb75116d35fc69972aa52d04eb7f66c76e261d89446b4eeab8c178875d07`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 21 May 2026 22:56:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 May 2026 22:56:32 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 22:56:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 May 2026 22:56:34 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 22:56:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64'; 			sha256='f1332ddb9010bd0b72628266c3a906d9a6979848033df4c8d9bd2cd113bae12b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v6'; 			sha256='1f6c8a082281706a0b9e24b64b9210ca0df5273ceaf600536012e7a62d790538'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm-v7'; 			sha256='ad4e0938c94638ac882641b924f6eff6889cc59a11f062e733cf337458aa6f35'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-arm64'; 			sha256='c34e32dd6ea2653d960d6c099c9f09b9077e4a37504d2d31e5066eccc3904231'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-ppc64le'; 			sha256='a509dc17005a4eee3568336d9e2479642e53b31110e039a8f5b4e6079744d0e2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-riscv64'; 			sha256='c2cf15773a0610e6de34a04e9191b07915d0ea2afb381a37ac87f0dcb213b85a'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-s390x'; 			sha256='edb0e83d5a2fa8913d0af46385b648408b4776ee3241b4c15f92fcadbc72b550'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 May 2026 22:56:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 22:56:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-x86_64'; 			sha256='33b208d7e76639db742fae84b966cc01dacae58ca3fc4dabbc907045aefdf0c4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv6'; 			sha256='38c8b500e75de30707024db9d135af979f4fdf6b9bae82b7a854b17eddad1205'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-armv7'; 			sha256='5cce4229012b8b18067fba078c9ec4e2a5dd47cb4cb3a0cc3d431f6fc429060f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-aarch64'; 			sha256='d4fb48b72857810314d3ee77123c89954101844efa4788031221f4c370495946'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-ppc64le'; 			sha256='044a5a6eac8ba3b686e5ad74d529293372eb6d8553685738fe93ae6a6fd92790'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-riscv64'; 			sha256='03565cf8e16b3afa6fd6555d697b3237ea2d4dbd5547ab6835bc90fa7e5e00bb'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-linux-s390x'; 			sha256='5bd0db672b07bb86272e84bbddd286f42fe9b84080e4d47ad3a91a84bd8c2c3d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 May 2026 22:56:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 May 2026 22:56:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 May 2026 22:56:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:56:36 GMT
CMD ["sh"]
# Fri, 22 May 2026 00:09:56 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 22 May 2026 00:09:57 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 22 May 2026 00:09:57 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 22 May 2026 00:10:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.5.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.5.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 22 May 2026 00:10:01 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 22 May 2026 00:10:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 22 May 2026 00:10:01 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 May 2026 00:10:01 GMT
VOLUME [/var/lib/docker]
# Fri, 22 May 2026 00:10:01 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 22 May 2026 00:10:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 22 May 2026 00:10:01 GMT
CMD []
# Fri, 22 May 2026 01:10:05 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Fri, 22 May 2026 01:10:05 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 22 May 2026 01:10:05 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 22 May 2026 01:10:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.5.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.5.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 	; 	rm rootless.tgz; 		rootlesskit --version # buildkit
# Fri, 22 May 2026 01:10:06 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 22 May 2026 01:10:06 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 22 May 2026 01:10:06 GMT
USER rootless
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae988a6da12e07a4495206223708dfa12193c715305da0959269e07cfe0883c`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 8.4 MB (8368391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad63753001c8116da8d4078088f8c226c9d2d5ebb32c543695bad3dfd05cb848`  
		Last Modified: Thu, 21 May 2026 22:56:42 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1523489b9bcf5899f4ec01d3ea4b3b09a7f11127bd6cfac3ad985d4e121a917`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 18.0 MB (18003804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4276c1b3c4ca523a976f2b634bcd7b921a29dbff4274ac9aa9cc1e68ed96f93`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 20.8 MB (20815981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e3a6fedf4004b1aba4e7b35c15a75f4e30fd0ae9d353199415f18fd99a7cf8`  
		Last Modified: Thu, 21 May 2026 22:56:43 GMT  
		Size: 10.4 MB (10359860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37af9029ae6a6376f88d713b9b54fb69ece2959cf06985f67d3905c6ef36739`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df60bc257eb03677643450dfa9477ebdad3b524820a408218637a85932c45d`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe07c252ff4b96737716f829e1e8ff46a81625412f850d98480be21cf51f845`  
		Last Modified: Thu, 21 May 2026 22:56:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a46d70ede680ec672d8f5f2c9bb5af48a2c9a43681a21842d14677a0b82c662`  
		Last Modified: Fri, 22 May 2026 00:10:11 GMT  
		Size: 7.2 MB (7219872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de27391729b9c976c43909efe6c9bd4bd3d085af7f1486fef0bd572f271852`  
		Last Modified: Fri, 22 May 2026 00:10:11 GMT  
		Size: 100.9 KB (100931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12385497f4dd0e48dee7bf5d61c0a58f3c9dbec80e8aa4a53a3f7be159ee8184`  
		Last Modified: Fri, 22 May 2026 00:10:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e676537b5027ea44a0661be403c5e6e90eaa2fa449a907d805f2f0c224a8e010`  
		Last Modified: Fri, 22 May 2026 00:10:13 GMT  
		Size: 62.1 MB (62129884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2b6cd64488652b8c6343fc20f1aebdf11fd687c16c86cd0ce33b02c753d758`  
		Last Modified: Fri, 22 May 2026 00:10:12 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c031f8f9a7062748f76bdcfd5b0a1cc8cbac8ceee0f7bdb6f4bd484e0cde4c`  
		Last Modified: Fri, 22 May 2026 00:10:12 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6d118403f244b706e4942321d1c4e66a03c146f9a8062898d767cb4c8b323`  
		Last Modified: Fri, 22 May 2026 01:10:12 GMT  
		Size: 3.4 MB (3394560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0897d676ba40602d3240ab261e7e14aa2762bbd0a1bf7368ccd81cb1f9c7cff`  
		Last Modified: Fri, 22 May 2026 01:10:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97396719cbd9d51ea1e3506925a8a5a115d8ae58c81838e8c6ad51c314366a40`  
		Last Modified: Fri, 22 May 2026 01:10:12 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643b7d89cde598c916bf7c7f00e93dc5a36e8c1d91b2a6569edcec53aaea6dcd`  
		Last Modified: Fri, 22 May 2026 01:10:12 GMT  
		Size: 11.2 MB (11236505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf756747af86a3f863daa1d517cb546bd5d301b9fedaedd8ea9d15714711f419`  
		Last Modified: Fri, 22 May 2026 01:10:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9e112f6b3fea966df90f157def05e9518958d5140f10f9e7071454176cd7efcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8b70e5e3140da514fa4cecbe47f54db15ab7e94c387f75740722aa8fc0fdc6`

```dockerfile
```

-	Layers:
	-	`sha256:d245ffab70d798025c3ee99ca69df635ceaa3d4fa4961cf7eb862863b47a3218`  
		Last Modified: Fri, 22 May 2026 01:10:11 GMT  
		Size: 30.7 KB (30662 bytes)  
		MIME: application/vnd.in-toto+json

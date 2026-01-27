## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:438cc9fb790caae654a29f2abdbe48bc2713f4bacc2bd412b7d2c60e458dd7e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d996fddf7545f36bb88186f0f93d91be8a344f66e1bf533963ef43af9f55ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164593926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13178a6a1a242b18e6c4d5026ea85091f37708edeb65a4c272ae38f5c5625ffc`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:19:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:19:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:19:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:19:16 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:19:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:19:17 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:19:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:19:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:19:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:19:18 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:11:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:11:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:11:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:11:06 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:11:06 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:11:06 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:11:06 GMT
CMD []
# Tue, 27 Jan 2026 00:10:27 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 27 Jan 2026 00:10:27 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Jan 2026 00:10:27 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Jan 2026 00:10:28 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Jan 2026 00:10:28 GMT
USER rootless
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd81c2978c1332d61e1f8b5343a99f7721f7d0b603e842a1fd6c0c7f65639f7`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 8.4 MB (8399628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf2cec19992fff6202960cf4dd658e26fd38397de7c1569ea74bf942ac0b299`  
		Last Modified: Mon, 26 Jan 2026 22:19:25 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a027ab1f50d1661d989d1aa5934de12f92bde42f1a94da3ef1b252ad539853c`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 18.8 MB (18774052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bbb99194498b5fad9a835784df5183b1eeac6f7ee5732f5db0c933b720ef7`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 28.3 MB (28308916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e225819afe03923d2ca6e8edde2df0963667a8635b6d3f2dcc1b0645bd0e6947`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 10.8 MB (10799765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e857b4c66d91aabd289aebaea5265319f76bf3fcc0b46fda3cfce9a823145f2`  
		Last Modified: Mon, 26 Jan 2026 22:19:26 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498c744a0f5728346169c842952c79c3b5b57408c7193c8301fc4963b7b4d16`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787bf046b98710a9f996308a88684f931b8d4dede08e93b0c2534dd85f045e91`  
		Last Modified: Mon, 26 Jan 2026 22:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0f3a97bc6159c7969cb8d24defc575a1700b3a180d55064fb7e0568d294dd`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 6.9 MB (6934123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b77ea85c6aa382424f1a4ab6fbbfdb6e8391ddf5e2aef9e553edf08fd87be5e`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 92.5 KB (92459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e02c98568abbe0d5183a689d36d64db6c84d30ab6d8b20879b53fdeb41ddc`  
		Last Modified: Mon, 26 Jan 2026 23:11:17 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d13d7c3ccdff7f976f45a8c03c3c629690a5776a6578075c818be4d5be3a7`  
		Last Modified: Mon, 26 Jan 2026 23:11:19 GMT  
		Size: 66.6 MB (66619580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff703f78a3b1870d9e45b2aa3741c77ec4e9971d4bd414514a2c8a243da24a4`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2450301eff05fb36fd677b935af7cdfe5b20cb4e6f62d00a5131b552b96d5bc`  
		Last Modified: Mon, 26 Jan 2026 23:11:18 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fe2f1fa32645d48d001a89d38a430aadf23b75f1d0e5ac13f1b01167cb9832`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 3.4 MB (3419926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa627d12989120878617b0ff6a40178ee7aa2784f5f2458842b19940aa939d`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a31c2a645fd1fcc13c6428f0ac8ac05191dbdc4e0f1b4534d0d55200cbd33f`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aadcb781d1119f67cfaa92f5bde31a037fe5d04e96a4c69e91c34cfab5cb01`  
		Last Modified: Tue, 27 Jan 2026 00:10:34 GMT  
		Size: 17.4 MB (17375881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909a4911b0841bb43582f002f95adfb02250cfbb041acf646784c23c49170dc0`  
		Last Modified: Tue, 27 Jan 2026 00:10:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:eecdfcfd5d851df2dcb6b062c1bcae9d817e4341b90becdf8d55e6507a44f25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c62ce9d4e97e2653e88e62ec6e16475ab34150bd8b5bc28726aa2540e7836a`

```dockerfile
```

-	Layers:
	-	`sha256:c25d5569116a154c4af8fb0680af4fc57f9c5115376f49cd584c859895dd7b2b`  
		Last Modified: Tue, 27 Jan 2026 00:10:33 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b1e508668ee940f39e31e6a4628b6f9a0e413322a092f5331f669f2b3e20d5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154353821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a552b8a628d1f17e4a8efdedba1acc4ba1ceccd944139be93f60b8792dca72`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:15:24 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 26 Jan 2026 22:15:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_VERSION=29.2.0
# Mon, 26 Jan 2026 22:15:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 26 Jan 2026 22:15:27 GMT
ENV DOCKER_BUILDX_VERSION=0.31.0
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-amd64'; 			sha256='39cc424a730d8b7364c23a137582cb29e7f024b175bb595001ff6f90121b005b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v6'; 			sha256='fad601a520d9da32ff72d5f844c08318bb66db7a9c150e01541170e4e275a724'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm-v7'; 			sha256='68f3aff3e29d9c013a90bec8cd841a86d57670394870fe0aaaceafcdd28f4071'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-arm64'; 			sha256='3192d6deafed620132da1acd7c68499e163c814bc2be988a3eb2c5302764a30a'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-ppc64le'; 			sha256='fe18282ceb82368e3b7fd79277e34d9904dfbfd0318a3c9fa2e4a2ab12f932e6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-riscv64'; 			sha256='bb01f095fb6b3734e352c4f58b7ef294f054d990c899fbfcaf5aa3fe1efbd83c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.0/buildx-v0.31.0.linux-s390x'; 			sha256='b03b64ab619c073edbaa310d83f275c52b7380abf080d35ea936696eab42aba1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Mon, 26 Jan 2026 22:15:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:15:28 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 26 Jan 2026 22:15:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 26 Jan 2026 22:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jan 2026 22:15:29 GMT
CMD ["sh"]
# Mon, 26 Jan 2026 23:10:28 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 26 Jan 2026 23:10:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 26 Jan 2026 23:10:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 23:10:32 GMT
VOLUME [/var/lib/docker]
# Mon, 26 Jan 2026 23:10:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 26 Jan 2026 23:10:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 26 Jan 2026 23:10:32 GMT
CMD []
# Tue, 27 Jan 2026 00:09:56 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 27 Jan 2026 00:09:57 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 27 Jan 2026 00:09:57 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 27 Jan 2026 00:09:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 27 Jan 2026 00:09:58 GMT
USER rootless
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f78cecd3cea41fb7bfc8571ede11309eec179c997fee1b8173cbec5832eef7`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 8.5 MB (8453538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fe044a223d3f0c5e702e1e34965ab791d4b26b0b9bdd3139eee120e53a151`  
		Last Modified: Mon, 26 Jan 2026 22:15:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a5135ddec2b78e338e29a47f853d5fef74f6c2936ab3bab18385c5358084c`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 17.3 MB (17349910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6cff33d2adb7a97c8a415ba5d948c014bd14333ff6e4483f2d8ba8bc98ff0`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 25.5 MB (25539739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2896a1cbcfd162f1738f4eca6a8367477c5a27eb5936586a805e0b3cf1949f41`  
		Last Modified: Mon, 26 Jan 2026 22:15:36 GMT  
		Size: 10.0 MB (9954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908bd72f7bfe569de359a4562f494f1f168c2a0af9f9bbad198fd4cd9cb6f286`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a2e4c42a69869d13646379197cfa1afb145e82c03fd83646879305ce771804`  
		Last Modified: Mon, 26 Jan 2026 22:15:37 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1edac0782aaaa5fc65761e914c5d5d107e15b7f3eb109b3dc6959e4eca1141`  
		Last Modified: Mon, 26 Jan 2026 22:15:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5329329b6918d115d8a37506fd2431c21b6298cd94a9b208da35fb003740fc62`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 7.2 MB (7213044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433c5f7f284c103dc5a82b1d914b49b4a93985d2d38d90e525fdd85fa1ce74cf`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 101.3 KB (101284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698fe5b07154cb7972a5bb43282c3aad803457a392010c85f5b62b4ec85bca`  
		Last Modified: Mon, 26 Jan 2026 23:10:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee4fe54b27540af7cc65175b5dc47ba526c54161e03e4aa695c2d4cfb2788a`  
		Last Modified: Mon, 26 Jan 2026 23:10:44 GMT  
		Size: 60.4 MB (60431702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb04c44549ab1c45ea75ba9f22ed6a1be7889ce70f1d4ba7acb333180173c4b`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd37aa3a15b0c51e88ac58a4a2af99cbdb09ebb96821e2375cf0884ec6b6f2`  
		Last Modified: Mon, 26 Jan 2026 23:10:43 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdb84c2218b48c5b9766cb97850e54d443b737e5e4530a3f38c489d7e8f4089`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 3.4 MB (3394372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412d57bda1cb43b60c1cc6a6fb3714df5f8210c32786cc45199eeee8cbdc14de`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e18bfd676e1a7766203504fd22927105c9de3a71a993ba1db8736ea1edeb25`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b129068910c279c84e85bc7ac66a57ed83092823bb7f7c6472e14dd0b3e2a5e8`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 17.7 MB (17710524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706f08ecf2c655ec8c075aee1b4e8927526ca15e209be5619b920a56c0f2b74a`  
		Last Modified: Tue, 27 Jan 2026 00:10:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ee2d83c7bb434663d31bce1757b12c86071167fc765d1b6c6d7ee002f8eb0be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f5d2f47b1b608f50f1efb950866fd3f2f97cf8b013382b80ce6952b1cd4171`

```dockerfile
```

-	Layers:
	-	`sha256:48499ecd27366c720d757644ac58e98c7a3843f0e5128ab6ea6487df0f704a8d`  
		Last Modified: Tue, 27 Jan 2026 00:10:04 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

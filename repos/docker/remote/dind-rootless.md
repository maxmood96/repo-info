## `docker:dind-rootless`

```console
$ docker pull docker@sha256:ad4962f1c2dba4d21b0ba1e843470e54163f1d58ebe7c0771bbf4d96775157df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d50df6a0987bbf8f1f492a4178c37e69ecef298e833910e1e544f6d48cfe2f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149707075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133463a7546ac69a908f56617f1a57871f63d95698327506d35ebc70cd6438a1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_VERSION=26.0.0
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 20 Mar 2024 21:16:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
CMD ["sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
VOLUME [/var/lib/docker]
# Wed, 20 Mar 2024 21:16:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 20 Mar 2024 21:16:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
CMD []
# Wed, 20 Mar 2024 21:16:36 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 20 Mar 2024 21:16:36 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873734828ac0a6c7f34d1db172b2f0030fdb435df5146586fd6a5d51b814396b`  
		Last Modified: Mon, 01 Apr 2024 23:51:09 GMT  
		Size: 2.0 MB (2026148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346ddc1c5c7c08e87cd08032481a09ee7cdbb4ca531949d09d28cc9655ace49c`  
		Last Modified: Mon, 01 Apr 2024 23:49:41 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9142d356271bae6a04d03aa685915516150702b3b3e0b0dd32f9a79959f6207d`  
		Last Modified: Mon, 01 Apr 2024 23:51:09 GMT  
		Size: 17.0 MB (16973517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15b2c839cb13b1bd756f6a20aaa9be1f22c63f887ffc22deb214e48c5f4e3c4`  
		Last Modified: Mon, 01 Apr 2024 23:51:09 GMT  
		Size: 18.0 MB (17982276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af45dc8672ce75af37ffa42eed79743cb0260be75f92f0c9cf297a9b759a94f`  
		Last Modified: Mon, 01 Apr 2024 23:51:09 GMT  
		Size: 18.7 MB (18669520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fabdcdd6e59ed89e307bd1db92cf13cf75f57f6ab840c434dcf992933b2b3f7`  
		Last Modified: Mon, 01 Apr 2024 23:51:10 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947a133a0a5efdbc2dff4e703c6741e23bccc9e84c75a27be26cc670ac60b030`  
		Last Modified: Mon, 01 Apr 2024 23:51:10 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e088f0fb3321c435828e6bdf213bc930dbf31df1e2c14b6b28883a6549b0d186`  
		Last Modified: Mon, 01 Apr 2024 23:51:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d175778f47860a60d940a27a0e8416300239d72ef4d05bdf369ae3731fc701af`  
		Last Modified: Tue, 02 Apr 2024 00:49:33 GMT  
		Size: 12.2 MB (12164496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca9b419913bdc88484a08ad8b2225b030989f9ca9c38a013bf3d8672ab1de51`  
		Last Modified: Tue, 02 Apr 2024 00:49:33 GMT  
		Size: 89.1 KB (89136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43377f19d2e00685818b6cf3971c020554b34d1946a54a690409ff5ab5ca3be6`  
		Last Modified: Tue, 02 Apr 2024 00:49:33 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc468b2772ee59a9aa65979664411f5efa7d766106b0824806d7bfe4b449bea3`  
		Last Modified: Tue, 02 Apr 2024 00:49:35 GMT  
		Size: 56.4 MB (56415804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5b066ea29c6ea36fc6c2d01fc851701e7407951b5b6791a9bc156e3b3798e7`  
		Last Modified: Tue, 02 Apr 2024 00:49:34 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd911e10e30b0200688a50fa2da32fc872c9a328a6140f2024115f2e66b13422`  
		Last Modified: Tue, 02 Apr 2024 00:49:34 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9aa5e59e35f334273ed553d06e36f72567f0f1b54d5689e7e9cd4f9516a892`  
		Last Modified: Tue, 02 Apr 2024 01:48:42 GMT  
		Size: 981.6 KB (981573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce61eed3d827da2177202de2372abcbf484dae15c854f1ad8ffa94c95198a0c`  
		Last Modified: Tue, 02 Apr 2024 01:48:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d07fd871d4921a8b1381fa8eba52d9921ea56548f92e39bcfe8bfe849e147`  
		Last Modified: Tue, 02 Apr 2024 01:48:43 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4116fb388f1c2ce5e7474f307dc944ef7ce1f2c85e9077266226a48a80b6c32a`  
		Last Modified: Tue, 02 Apr 2024 01:48:43 GMT  
		Size: 21.0 MB (20985920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a0e1b0c5b452dd3d3efb9eee5045f42bf451e9f3a31c2305de1b830dd055dc`  
		Last Modified: Tue, 02 Apr 2024 01:48:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a0681a0c111ee20e66f9bb7ba486da240a57e95db2fe03190bfe7120f0d5b463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.9 KB (906928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57dc8341d02ab0a3e7426d01ea6b076e6ec8b4db6fe290db0a1056b2916019b`

```dockerfile
```

-	Layers:
	-	`sha256:9acd147cdf81a1111c5539d5a9d279c2fd93b615a78e14e2fc76bf3e89433647`  
		Last Modified: Tue, 02 Apr 2024 01:48:42 GMT  
		Size: 873.7 KB (873672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f9eb7e2f7e831c03513243e2c6049216e219800ca308dc6ca9073e93688aa5`  
		Last Modified: Tue, 02 Apr 2024 01:48:42 GMT  
		Size: 33.3 KB (33256 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6a2b98fa9f651d306f2b42b0b1bd3030f5d2dcb4022ca0175811ef4e255fc5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143397948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb88d5203890c9d390a8f00e7fd657eaadbe46f6f66a8388aa67f28e60e819d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_VERSION=26.0.0
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.0
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-x86_64'; 			sha256='59c6b262bedc4a02f46c8400e830e660935684899c770c3f5e804a2b7079fc16'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv6'; 			sha256='97dac0aa10961ea30a79f6fe2c4a13bfe4da562926365a63042fcceb88d9d125'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-armv7'; 			sha256='d607ed69f5fe92ee1fd831cf764f977174c86192957a4de678c01db671c3dc52'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-aarch64'; 			sha256='6f00ed24a846046b441c0f0a0f8c1e00194f4b0e33f2433fac0d2dd0e486fc80'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-ppc64le'; 			sha256='e3afa6956f6cd4fdbaa8fe19781ae07a1bb8fb2f4d54a1aac857090d6fe1710d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-riscv64'; 			sha256='1d080f5bc04b4b97c61ce3f57ff4a7bd11299f486bc287833f162360be201a7d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.0/docker-compose-linux-s390x'; 			sha256='5f302fb8e7d973b53f1f9dc808d2b1af08f94687cb14b3f26cc7b358854184b5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 20 Mar 2024 21:16:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
CMD ["sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
VOLUME [/var/lib/docker]
# Wed, 20 Mar 2024 21:16:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 20 Mar 2024 21:16:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 20 Mar 2024 21:16:36 GMT
CMD []
# Wed, 20 Mar 2024 21:16:36 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 20 Mar 2024 21:16:36 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 20 Mar 2024 21:16:36 GMT
USER rootless
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b275a3377f65492f727dc46aa2b70be6ec8ff96583fcd9a7b699692b5170bc`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 2.0 MB (2019704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c53acdebd8fb391eae546ed72149f049f8ab4d594f12c74c49be04cc3b9708`  
		Last Modified: Sat, 16 Mar 2024 04:06:08 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eaffe3eb71643155936daeaa1598d665bd3ce7e4cd7ce7540eda599ce5e7fe`  
		Last Modified: Thu, 21 Mar 2024 00:17:46 GMT  
		Size: 16.0 MB (15983712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee06d9bd87570975d69f1b498d43c5d73ee2272dc95ec1a0ef1cf417a2b4e81`  
		Last Modified: Thu, 21 Mar 2024 00:17:45 GMT  
		Size: 16.3 MB (16349527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1172287503895a29f7a27066f3d541d4edb368754c3a6aa3555f6f5e783bd893`  
		Last Modified: Mon, 25 Mar 2024 19:11:37 GMT  
		Size: 17.0 MB (17046172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28cda27aeb58e151f6347653aaa6582fef35c655140f6d2a6cddc9fafec2cba`  
		Last Modified: Mon, 25 Mar 2024 19:11:36 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff57bb0e39d9ba044b2015dd11c7b4972b2e49e12e5969181f6da81f8c0402e1`  
		Last Modified: Mon, 25 Mar 2024 19:11:37 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cde276bbe4ee1509df387ac8a92f4b6aeb60b25f76f8db835e917d494790ce`  
		Last Modified: Mon, 25 Mar 2024 19:11:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551f321af971889f777209a3119010da6252756b5881e57a5ac31942e3ab0389`  
		Last Modified: Mon, 25 Mar 2024 22:42:24 GMT  
		Size: 12.6 MB (12631530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68618b928e74cd77a6095de0d1377ee1803562334dd55d5133edb26f6db281c1`  
		Last Modified: Mon, 25 Mar 2024 22:42:23 GMT  
		Size: 98.4 KB (98394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c369fbd592d4d0532c0741880ab8d7d5d348e5ac136194695da6b844844a8ae`  
		Last Modified: Mon, 25 Mar 2024 22:42:23 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d7aaaa7dbd7441234d4b55f8c692358249279c76ecfeebbb9de0e383317ee6`  
		Last Modified: Mon, 25 Mar 2024 22:42:25 GMT  
		Size: 52.1 MB (52050081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2b8e4d93ed3061100bb11838476c25fb1c7671232167e283f539244601058f`  
		Last Modified: Mon, 25 Mar 2024 22:42:24 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e2c79d62df216cded1f06dfd5a94458282d2ab612eaa3b36dd01540d0bd9b9`  
		Last Modified: Mon, 25 Mar 2024 22:42:24 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa0ae0e5e8183161ce0b2df890b11809eba0cdab1829b6d0e7143a2ec69cc0`  
		Last Modified: Tue, 26 Mar 2024 01:01:01 GMT  
		Size: 1.0 MB (1022497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f2781beb26b420a8c6e51d7a13e936312d9643389cddcb192d131d9b245f5e`  
		Last Modified: Tue, 26 Mar 2024 01:01:01 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfce7710c279e5ca77f5e6979aee7ac63bec1f3f8e91126343c6dd96807559e`  
		Last Modified: Tue, 26 Mar 2024 01:01:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c5d6f62d3d12cab082dad7fc16ad489ce4f875517599c40eaeacd89318949d`  
		Last Modified: Tue, 26 Mar 2024 01:01:02 GMT  
		Size: 22.8 MB (22838646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5f0d28331476c782eac1c73614511b23a83580c34698dacbb6d1ab2cec8325`  
		Last Modified: Tue, 26 Mar 2024 01:01:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6514ac6c59ab270a5df409fcfa0bf523a8a378391ab9a2e9f7fcc947953704ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **898.9 KB (898876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c4094616a31a25e89c03be781994da6b6824fe23d0b87b03f00219640b9283`

```dockerfile
```

-	Layers:
	-	`sha256:38a1457e6c2fa7302a6046f4f8fecc675694281bbbcdd1fbe94838de61483b0b`  
		Last Modified: Tue, 26 Mar 2024 01:01:00 GMT  
		Size: 865.6 KB (865557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b913cbb6b13e3118ede30d5baebb269bf8f0c9d3b742b1fb8063841cbfd1fed8`  
		Last Modified: Tue, 26 Mar 2024 01:01:00 GMT  
		Size: 33.3 KB (33319 bytes)  
		MIME: application/vnd.in-toto+json

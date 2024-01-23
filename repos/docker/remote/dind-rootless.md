## `docker:dind-rootless`

```console
$ docker pull docker@sha256:d7e4e0110d86839e17258ab57c45a865176c55384fe101b30c1ad4317eaaafa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:02ebc4abeeb07b159a0e80411f23efdf681955a6ae90522c149db7b25b4c0b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144628072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e7531a743dac1a5d90df6d436cedb326902995763ceab3e561decd662132d1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_VERSION=25.0.0
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.2
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-x86_64'; 			sha256='067a12983b9333d01947329190af756b6d12afe7b4b51b3e1e29328b4afe3b9f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv6'; 			sha256='582d734ef0c14335ee4691f3550d56b3e1c1c4d787ed6354830b3c222eee542e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv7'; 			sha256='e83fa84dc73cc8d5a0fe2d1ad3ad61202050f033e6df9f3f4f7b3c2b59181006'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-aarch64'; 			sha256='beafe762fedd06fe9885317c33f8b29b39c2354d6840a494a69b3c3a36919212'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-ppc64le'; 			sha256='6be73d6597efc822eff3f9dd6abb56b72ada76f8a5f798b1df2dce5105f39257'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-riscv64'; 			sha256='33a15fcef9d975aee4ed404779fae068264da6de8f2851ead85f9e1701302411'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-s390x'; 			sha256='0b62a8d7aad7ce81220a4d77aa4b17e443b888248c1da22bc808db1fcbf1e9ac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jan 2024 12:04:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
CMD ["sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jan 2024 12:04:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jan 2024 12:04:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
CMD []
# Fri, 19 Jan 2024 12:04:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 19 Jan 2024 12:04:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99fecc646a5691be8226c22d5248cb6f9332cdd8d03b2813a53923bb6e1877d`  
		Last Modified: Mon, 22 Jan 2024 22:50:02 GMT  
		Size: 2.0 MB (2018465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893d3febe591f94c7054aff6f650f5c5a44dd86d2559ad91aa401eb51c9b228e`  
		Last Modified: Mon, 22 Jan 2024 22:50:01 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc11cf79467c2396782fe79ab0dddcb2a4651a129d862c10736348a3bb90676`  
		Last Modified: Mon, 22 Jan 2024 22:50:02 GMT  
		Size: 16.9 MB (16894259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c541db7b3bb6fda7809dbe93d93ca00685baf5e9c554b213ccd9aace6368ee1c`  
		Last Modified: Mon, 22 Jan 2024 22:50:03 GMT  
		Size: 17.2 MB (17195294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802cf11ebfb4ba794cfb0c613511bdd6927ddc13a20660c78be4790e8f4da5f0`  
		Last Modified: Mon, 22 Jan 2024 22:50:03 GMT  
		Size: 18.2 MB (18175508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05773fd6f3c0c28805bb9f2d6d586fef02c44d0cf25f8e4eb296c1b33a99655f`  
		Last Modified: Mon, 22 Jan 2024 22:50:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886efdf86c556b40e0929438c85d489fde709389f6e4d70099ce9099e94db6a8`  
		Last Modified: Mon, 22 Jan 2024 22:50:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1604244e76aac43af382a2eb7d7e4d4440c35114f4f2fab0865d9e29e21e6ab`  
		Last Modified: Mon, 22 Jan 2024 22:50:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c42af7dec87ef5f0b5b3f9289f84870055b7be206cb842277173ca538295af7`  
		Last Modified: Mon, 22 Jan 2024 23:49:59 GMT  
		Size: 9.3 MB (9258273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cc785c2be64fc0886124f42b6ab9f4d161c9e0e47b3440b7e6a5469b20b164`  
		Last Modified: Mon, 22 Jan 2024 23:49:59 GMT  
		Size: 83.6 KB (83645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b464165c77525700b437f1a2e28ab2d02e7fec53507e2c82f188b05b8bc343`  
		Last Modified: Mon, 22 Jan 2024 23:49:59 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7f9c2ffbe982a87dc319073fa84f4f287ce41debea0376b2e74626d00e70e2`  
		Last Modified: Mon, 22 Jan 2024 23:50:02 GMT  
		Size: 55.6 MB (55631657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea349de5085ab87ee4c700f2723c98c3955179a66e46a09433544a50f8900daa`  
		Last Modified: Mon, 22 Jan 2024 23:50:00 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69510923d28c04476929b21a2b57c2e403152b532f5985f4e6bdfd26db07df2d`  
		Last Modified: Mon, 22 Jan 2024 23:50:00 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10c6d4d498560083d65e884becd4decc60823fde647e708fe0a1ac5ed3257f5`  
		Last Modified: Tue, 23 Jan 2024 00:48:50 GMT  
		Size: 974.0 KB (974048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70201c7994988b0c2fceda1bc295df62b9ca6538a8b7b0d8523f6b66e50fef4`  
		Last Modified: Tue, 23 Jan 2024 00:48:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5853460cc95490eef82bc3f14c5b4789296b4c2218d34265c3d20dded5a142`  
		Last Modified: Tue, 23 Jan 2024 00:48:50 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f7c3cb2b7557b77447ba8f72c10f37cf2bb952fea35057975c90f307795d0a`  
		Last Modified: Tue, 23 Jan 2024 00:48:50 GMT  
		Size: 21.0 MB (20978493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc492180324855e3a06426ba1b9ef9df4ed40c00370726e30e0c26cd6d69c91`  
		Last Modified: Tue, 23 Jan 2024 00:48:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:632e65949c54af3de2b81ee7c4d7aad28cd6bdb050b89565d9b0ee651362cef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253330ecfaacc5a2e0c9924e67d7f79cae73a920247e4cf3765f521186a1d099`

```dockerfile
```

-	Layers:
	-	`sha256:96e7137bdd84a3916f6454ffd5d6376a0025372b3e9f36af93d3d0de78e83dbe`  
		Last Modified: Tue, 23 Jan 2024 00:48:50 GMT  
		Size: 736.5 KB (736509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05258181815c5bfc3e3b4174f2fc3b55f828ab8fa6e4e726bda5ae4527129c63`  
		Last Modified: Tue, 23 Jan 2024 00:48:50 GMT  
		Size: 33.2 KB (33249 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ef6eb7a01b8b594c092ec64cead9098cf4838ae99ac047fb67ec44e1cc966163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138319831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74227f96677bce8a50200267e093ddb674b70d234133d01c0e1e9684ad079c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_VERSION=25.0.0
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-x86_64'; 			sha256='d350bbbd1c74c0a8542193bd41881afea534b141c6a9d9a27b2f217e51d5c48c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv6'; 			sha256='4a89b48f6a758793d4b40b1ade7bd9e7e2e177e29f05f74abb3fde08f246f0c8'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv7'; 			sha256='2b339b900447394b0cc985d9be30782361828b615ce743c36a9674d4435a2fb9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-aarch64'; 			sha256='9b35494742cc54544cd3f67b162ebfb43435077f02556bfb5a7e1c543f0a2da7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-ppc64le'; 			sha256='68ce36587759f18a9daaf4a11af6db1ba9e4b7089a8062654de38f8b84506647'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-riscv64'; 			sha256='b28cbb99ba1ae9d7b1a4e5d6828a2c2a9b124db2d4f1d226aa71a1f2741aa056'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-s390x'; 			sha256='6177f40328d4004d37b7e422d102d765aeb03e24e202ca8b791a6c000be90665'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jan 2024 12:04:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
CMD ["sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jan 2024 12:04:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jan 2024 12:04:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
CMD []
# Fri, 19 Jan 2024 12:04:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 19 Jan 2024 12:04:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4959de38143abac793d31e4e8592696721305ff06281f8b9284aee380afcfe`  
		Last Modified: Thu, 14 Dec 2023 22:04:39 GMT  
		Size: 2.0 MB (2014899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf613c8d3eefad31faacee38beeedf68069e48ea01d8f083fa0a57ce343ed827`  
		Last Modified: Fri, 05 Jan 2024 02:15:00 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594895876a66f55998b0c3d9c175ec0cfa723898879d7fe8f837de3b0e9e01e6`  
		Last Modified: Fri, 19 Jan 2024 20:23:15 GMT  
		Size: 15.9 MB (15901598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5598890badaf41ad29ca6e7a62aecf9b18e64ff1308118644d6ecda191bee6ae`  
		Last Modified: Fri, 19 Jan 2024 20:23:14 GMT  
		Size: 15.6 MB (15640596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72e0c5c013142ab0f105384e856690145c739b4c62798a667ba44e8b100815b`  
		Last Modified: Fri, 19 Jan 2024 20:23:14 GMT  
		Size: 16.6 MB (16610364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1471633a84a6349cfeb08bf4b9e8879be2fdbdb8d55b489543be73d31bf91c57`  
		Last Modified: Fri, 19 Jan 2024 20:23:13 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64d5b7dddfb9901291c707c8b672a987b74197fe26a2a8c58747cf784a5c08d`  
		Last Modified: Fri, 19 Jan 2024 20:23:15 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934f51c79a118bc2c9ef86a286aee9f3c33f0c413bd6c9ffa6c949a71275b217`  
		Last Modified: Fri, 19 Jan 2024 20:23:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e62c66ee4db0c28bdd0a8d371e3034736195c22a9cfc2221c71fd75403feffe`  
		Last Modified: Fri, 19 Jan 2024 21:22:03 GMT  
		Size: 9.5 MB (9509863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b221b641f720e676dc1fe4410dbb9fbd8a397497ac9a35fa99b2a43cc96f6f9`  
		Last Modified: Fri, 19 Jan 2024 21:22:02 GMT  
		Size: 93.1 KB (93073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0686185000f25f48b2caaea5bba0d9a7c01edd8b1e365dd62827707ec488560`  
		Last Modified: Fri, 19 Jan 2024 21:22:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09e5717c3fbfa466bfb8a152c3718c081fb34db45e79fa281023aace028913d`  
		Last Modified: Fri, 19 Jan 2024 21:22:05 GMT  
		Size: 51.3 MB (51341152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d979313e9f9262364f038e05249664ce08e9ae049b5f4145a10b45fb64151f3`  
		Last Modified: Fri, 19 Jan 2024 21:22:03 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c9a49ec4c63595dcad7f349573111e79ea86a4345028cfd8f9ea1c4374f044`  
		Last Modified: Fri, 19 Jan 2024 21:22:04 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aead3f75e6b71d1fdcf2e9d755cdcf6a282b0d95dfd4cd0554455c401a13dd1`  
		Last Modified: Fri, 19 Jan 2024 22:19:22 GMT  
		Size: 1.0 MB (1016208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da487590a2c48e8c325e2929c6add65ca0e2bab064c16ca00ccfc73e25a762ab`  
		Last Modified: Fri, 19 Jan 2024 22:19:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd93a0055ba888a0a1609ecb3f3f369dfa00a10e6601cf7f7de1c9f19975308`  
		Last Modified: Fri, 19 Jan 2024 22:19:21 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e599129b5a3f13667516999c2273af1cab5b416243f8568bb6d30b73e95585`  
		Last Modified: Fri, 19 Jan 2024 22:19:23 GMT  
		Size: 22.8 MB (22834334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831b7396f008cb85362f244dffa4ef36a6ad6eeb791d8aec16b6afdfc0141834`  
		Last Modified: Fri, 19 Jan 2024 22:19:22 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:95ffd48231f6e6095cdb5b31beb8010c8a4b36326dbb45ba240920acc372c20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.2 KB (770220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea06522332cf51d6b4b28598b0a3f47737d3bbd9c2f0d081ff3b6c01b46a728`

```dockerfile
```

-	Layers:
	-	`sha256:93fc37e909930c01560d45d909a7b10b500dd94cc9d3cc40f2328e975f1c7765`  
		Last Modified: Fri, 19 Jan 2024 22:19:21 GMT  
		Size: 736.9 KB (736908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00af50ce76ad49fcbbe02ce7e1e886bd457d0fc8070d8019d8cd22464084d5fe`  
		Last Modified: Fri, 19 Jan 2024 22:19:21 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json

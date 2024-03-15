## `docker:dind-rootless`

```console
$ docker pull docker@sha256:e798534508734e39198656a3cce12df6a64627be190de981c33aa5e1d7b68540
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:cbdfe9d4c58d004acb121b35bc1778506067ea53e3efc36a3afaf2dc1514887a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148408029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23e3dace0dcd3728ef7f93a58b8229cad9bfce344d24fcc7b25025f61ef0e54`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_VERSION=25.0.4
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 07 Mar 2024 12:04:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
CMD ["sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
VOLUME [/var/lib/docker]
# Thu, 07 Mar 2024 12:04:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 07 Mar 2024 12:04:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
CMD []
# Thu, 07 Mar 2024 12:04:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 07 Mar 2024 12:04:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf151956701dd021c86419e871db8b6747bd05af930a8b450c19930266d0edc`  
		Last Modified: Thu, 14 Mar 2024 17:49:04 GMT  
		Size: 2.0 MB (2018490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2bb9cdd6f31b926be90161ce11ba8000a430ed63159ab9c4d32e7a51c519b`  
		Last Modified: Thu, 14 Mar 2024 17:49:04 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33a16258cd20018b6e769bc45b8de7ea0f9417f4cd1f5a78a4adf28c73fdb06`  
		Last Modified: Thu, 14 Mar 2024 17:49:04 GMT  
		Size: 16.9 MB (16902847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2875dcb56416afe9a967bf8405c0e439930ee838f9dee3c299463e4cd283d428`  
		Last Modified: Thu, 14 Mar 2024 17:49:04 GMT  
		Size: 18.0 MB (17982283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360209ced14e200152b263c75bb77181f4c41aaefb63a3e9ef32e834893df99b`  
		Last Modified: Thu, 14 Mar 2024 17:49:05 GMT  
		Size: 18.2 MB (18214533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acbde70f38576dc2158e0fd0816023a7edb19a71885ac3f238556b80177a072`  
		Last Modified: Thu, 14 Mar 2024 17:49:05 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7094c34553da1fdaa92376231e440e8cc3299d688f5f5955132603b08f60fdb`  
		Last Modified: Thu, 14 Mar 2024 17:49:05 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e454e4b780ce8c0fd054f61647f57388deb6384c5f7422aac7783b3d1801e5`  
		Last Modified: Thu, 14 Mar 2024 17:49:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ab83a05af4737bc778d747aab3c6a0f768953d42d466f8a7700c469b25fd88`  
		Last Modified: Thu, 14 Mar 2024 18:49:15 GMT  
		Size: 12.2 MB (12155979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706a9b923a28142045ae7ecec5a788ded4f6efa69edd0bd5d15e20ccd7101de6`  
		Last Modified: Thu, 14 Mar 2024 18:49:15 GMT  
		Size: 88.9 KB (88864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bdcd159f55536a6f329ef7706ef4d92ab457cefbe6bd640db13216585c3130`  
		Last Modified: Thu, 14 Mar 2024 18:49:15 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5c12addbb7292a5c7981abcb711368a71cfab10ae00e7b647b1445ef8154be`  
		Last Modified: Thu, 14 Mar 2024 18:49:16 GMT  
		Size: 55.7 MB (55659131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bf9a92f3249f061ee6a6b27c68b4661b9b38175b1daec6054b2dd0e688eaf3`  
		Last Modified: Thu, 14 Mar 2024 18:49:16 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c166a377d301f696090dfb186658618e3baed04d4590b179abcc33ed54d3244b`  
		Last Modified: Thu, 14 Mar 2024 18:49:17 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8c6c832135a74d5e72b5ea76b4e8a339f52ade3bbba1556e4bd69203d5ee73`  
		Last Modified: Thu, 14 Mar 2024 19:48:14 GMT  
		Size: 981.3 KB (981299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89a73ae5fb909c16bdfc65932164a394c15eba282029535e49de5692219746`  
		Last Modified: Thu, 14 Mar 2024 19:48:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721f63a1a07529181502872afcbfe56997c87f4dd4dc0ab1fdc14e6cf29a67a0`  
		Last Modified: Thu, 14 Mar 2024 19:48:13 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b85120976eba6eb4c0c54de4c66806c655de891b9126e6619fdf3fa21a55295`  
		Last Modified: Thu, 14 Mar 2024 19:48:15 GMT  
		Size: 21.0 MB (20985916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8cffff5a4f0fbfedfa871db2b20bf8faa009dd192a3ba8e0017db0cdbe0a22`  
		Last Modified: Thu, 14 Mar 2024 19:48:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9be36adf929c94194dd66f475c6ca97ac75a7321165c46ec3dfd02890fa1bf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **918.2 KB (918211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04915653b4673cacaad4241251d3145833ce9d2e5b5244d446af6c177a97f067`

```dockerfile
```

-	Layers:
	-	`sha256:43a41f59aa3ee44f74bd6919f2d6ff11cd8f558e385a2c01062ac860a1d038d6`  
		Last Modified: Thu, 14 Mar 2024 19:48:13 GMT  
		Size: 885.0 KB (884955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8223390429115b0a339ff98956f62994441a02c5471d72dcea9a4eb968f1d9`  
		Last Modified: Thu, 14 Mar 2024 19:48:13 GMT  
		Size: 33.3 KB (33256 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4443f20a7354eee644b8936ae3dc8455b6cdffbf62c213d403be7d9f8816c169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142234388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9681e1ad69b5df3c5bf6c42a44da7296d188cef84357a299aac0030775314c49`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_VERSION=25.0.4
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-amd64'; 			sha256='ddd69ee2ca3dd61760e771dcd2f3453dc677dfeb42c9484cc2321b96bc1b7c57'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v6'; 			sha256='6aea498b2a168bcd13f919e85e0670c2e5a71abab8ecd6bfe52874d14680f617'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v7'; 			sha256='1566b6f3cf69d06ade467d9928e19f6a6682182fe3008bc9a0c83385d5637fa9'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm64'; 			sha256='fa36eb4deab2fac6ddf5fdeddcf16999bc9d5fb1d632e0ba7e572b519df8a656'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-ppc64le'; 			sha256='aced23b7832c690703d0cb6339d4ccdbac9b45f0392b865b131aba9b572ae3c1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-riscv64'; 			sha256='c15e51986d59398552b3ecd50b4ca75779e42c878e34761df54616ac02165207'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-s390x'; 			sha256='c3578ab9814e4c2d0f917721b1dfd140b85e40602f6128745178a051cf4d0196'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 07 Mar 2024 12:04:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
CMD ["sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
VOLUME [/var/lib/docker]
# Thu, 07 Mar 2024 12:04:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 07 Mar 2024 12:04:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
CMD []
# Thu, 07 Mar 2024 12:04:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 07 Mar 2024 12:04:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1445a503f72c73d6089a1119111ac23a281bc485cb856ca4679fe872c1a9ac8f`  
		Last Modified: Thu, 07 Mar 2024 18:50:58 GMT  
		Size: 2.0 MB (2019674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15768397550ab4bff548e50cb3f24c0a65a8e000b6e0f00a9930bd55c3889118`  
		Last Modified: Thu, 07 Mar 2024 18:50:57 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a732e1a4ab5b03c3cd91f94676d8a2d3b6a6b002dcc01f32a1ba805465a686`  
		Last Modified: Thu, 07 Mar 2024 18:51:29 GMT  
		Size: 15.9 MB (15907330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585f249362e56bfdd61e702eda2c2db4829de007ec706dbaa9e347c0d638e5c`  
		Last Modified: Thu, 07 Mar 2024 18:51:29 GMT  
		Size: 16.3 MB (16349453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd0945b801b77f63d5a5a6bae41a993c111686d68e4bdf828d4cea59770435a`  
		Last Modified: Thu, 07 Mar 2024 18:51:29 GMT  
		Size: 16.6 MB (16643005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10633038d357a7c3b8107d7cbef12bff14230fb3078d55ff2cde7822b51e9c36`  
		Last Modified: Thu, 07 Mar 2024 18:51:29 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e79eafdb91f705d1f3ffb77f80422a78fdd579c7c5e620b899e067938d1baf`  
		Last Modified: Thu, 07 Mar 2024 18:51:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1095b69416c8e4960e22536f273dd4f7eba8cc6fe13308276db2f90edbc2de0c`  
		Last Modified: Thu, 07 Mar 2024 18:51:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1e1c5b71d75508a1077f7998c23fb6861b99c4ae3d78611ea57def4d20cf8f`  
		Last Modified: Thu, 07 Mar 2024 22:00:53 GMT  
		Size: 12.6 MB (12627129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411ed5d80a13e460f951641223dfd49d1039537faf504791a64bfc558effe0a9`  
		Last Modified: Thu, 07 Mar 2024 22:00:53 GMT  
		Size: 98.4 KB (98382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5971634f397ed41af96d22a4c2a013db8b7fbcf0041ced273f7b6f0c544a4e3`  
		Last Modified: Thu, 07 Mar 2024 22:00:53 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2644a092a7d971928211f5459fa36dc0e1fae63eb4bf6cbe214348c2fc19d442`  
		Last Modified: Thu, 07 Mar 2024 22:00:55 GMT  
		Size: 51.4 MB (51370644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f2d6caebebc555bd07b64da94d258748182f47670e3f8995c12ba2d83e61b3`  
		Last Modified: Thu, 07 Mar 2024 22:00:54 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec19dabf82f62c565176c0128e5a725feec6a3cf31acc0b94317742612656eaa`  
		Last Modified: Thu, 07 Mar 2024 22:00:54 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da921d42c50be0f7d7ef4a027461a980987ba5e96093050da7c4d9baf4a5592a`  
		Last Modified: Thu, 07 Mar 2024 22:58:37 GMT  
		Size: 1.0 MB (1022484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ebee6a73049e358ccc77d5c6b76c2292fde87df1b854f1ff4dd6249502fb21`  
		Last Modified: Thu, 07 Mar 2024 22:58:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61e1ed5259f479f26761c337c29cfb7abb587c5cae4e98ddbb209b73362ad23`  
		Last Modified: Thu, 07 Mar 2024 22:58:37 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f006bb76bb7f820647bdc4ee007e8b76d6b74566771490e61172a7d4b97d4909`  
		Last Modified: Thu, 07 Mar 2024 22:58:38 GMT  
		Size: 22.8 MB (22838621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3e01474bf4cd62113472db5c4463361c35d57300fb51037625c24310c7e635`  
		Last Modified: Thu, 07 Mar 2024 22:58:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bfcd245aed2ddded4025a5ca6ecfcf38d8c984748338eb11df72e6856a4ceab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.0 KB (919034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e6963d8385d68ccfbc66b1a977cfcbb3ba2bb1530efe89b2a584140d364ad0`

```dockerfile
```

-	Layers:
	-	`sha256:e4d17b98477cfcec1981b76bbb6642e743e2a19414a8bdd17233132ad08865cf`  
		Last Modified: Thu, 07 Mar 2024 22:58:36 GMT  
		Size: 885.7 KB (885715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f481b74e443dff4e6eff31fdecca270dc232650c972dc6834c3fa9aa2bb76923`  
		Last Modified: Thu, 07 Mar 2024 22:58:36 GMT  
		Size: 33.3 KB (33319 bytes)  
		MIME: application/vnd.in-toto+json

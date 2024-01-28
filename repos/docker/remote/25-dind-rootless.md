## `docker:25-dind-rootless`

```console
$ docker pull docker@sha256:3f41e7131312e439465fe1d2e7a0f08bca87e09acc8316bed271954eb8489a14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:25-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6727290177f2b0a78a057310e1cb09f1884b8f4e9e324cacf2a315e955db16e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142441415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189433c465be7e3b6bf9c7fb5c6a9369d642e6170c1bac958949a78c9a838f9a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 24 Jan 2024 12:05:09 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 24 Jan 2024 12:05:09 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_VERSION=25.0.1
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 24 Jan 2024 12:05:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
CMD ["sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
VOLUME [/var/lib/docker]
# Wed, 24 Jan 2024 12:05:09 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 24 Jan 2024 12:05:09 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
CMD []
# Wed, 24 Jan 2024 12:05:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 24 Jan 2024 12:05:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b66001efd45f36ee9449cd675dcf2dde2ea7959080bbd796712392b65afdf6`  
		Last Modified: Sat, 27 Jan 2024 00:52:45 GMT  
		Size: 2.0 MB (2018441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0843e739335044eca8846db1d8b8247383d8e4fc8c2dbc4b5dd3701de7321b1b`  
		Last Modified: Sat, 27 Jan 2024 00:52:45 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fbbf900a6735bde4ce796d5431e7d9788f64b8705ab70d015919d287dff9e6`  
		Last Modified: Sat, 27 Jan 2024 00:52:45 GMT  
		Size: 16.9 MB (16894259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88603f4f47eb7a5a9b5feb5ada6dd0216d102e754d61ffbff6b456bd5009c18b`  
		Last Modified: Sat, 27 Jan 2024 00:52:46 GMT  
		Size: 17.2 MB (17195293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b84db2aa43f333006df5175860e9de483eb97569df802ecca0431444603e07d`  
		Last Modified: Sat, 27 Jan 2024 00:52:46 GMT  
		Size: 18.2 MB (18175351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac37d218d38040abebb0254d92a6b270ef49d883a48f18fd37d1af409d88f926`  
		Last Modified: Sat, 27 Jan 2024 00:52:46 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c94d3daeaba40a22fc72700b8e9ee851b37ec20a984a1e1fa658efbf060564`  
		Last Modified: Sat, 27 Jan 2024 00:52:47 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43cd6697a9a858f51bab587d9187d267c4fdff6719cf514919e60e9eb8481d`  
		Last Modified: Sat, 27 Jan 2024 00:52:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbc5d0241907b7cde23293eb1a02871fe05eefdb26d104fa038000a8d9d06ea`  
		Last Modified: Sat, 27 Jan 2024 01:53:38 GMT  
		Size: 7.1 MB (7068045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ea543efa6a4c8cdfeb91f116a91df0ecf462bf081974d060d098385df9eea1`  
		Last Modified: Sat, 27 Jan 2024 01:53:38 GMT  
		Size: 83.6 KB (83643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9460742e5659663f4c1589b644e75deed0292763f6eebd506a672a614d2d6a70`  
		Last Modified: Sat, 27 Jan 2024 01:53:38 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecde4f34493c85bd53c403015a9f5b555572b54632b0ac6fa7a3e7113c42869a`  
		Last Modified: Sat, 27 Jan 2024 01:53:39 GMT  
		Size: 55.6 MB (55635204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8515a1673a09a4dea7827b3d8b3bedbfe386ff020bedb21481c69a49c830f19`  
		Last Modified: Sat, 27 Jan 2024 01:53:39 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46ff24c683d41e94bc33eb07e8627856a69fb899db51a418c885d0fe4ff4c98`  
		Last Modified: Sat, 27 Jan 2024 01:53:39 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74df83c8daab427fb8c3028e1ef73c211f3f9375d44c62f3c36128048ded6637`  
		Last Modified: Sat, 27 Jan 2024 02:53:07 GMT  
		Size: 974.0 KB (974043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87998e322d9fc0a019e8bcd3e21b6b7d2fffbc39601a5ef8409efbaaf2761f95`  
		Last Modified: Sat, 27 Jan 2024 02:53:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2272ec322d62320dcc12608093d12505b78940508a54f925cea2deb21330cd`  
		Last Modified: Sat, 27 Jan 2024 02:53:07 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33bb2b6ebda15f9421a9c05167fcf98b9ceb396c0d0feffa79bcc61280e60b5`  
		Last Modified: Sat, 27 Jan 2024 02:53:08 GMT  
		Size: 21.0 MB (20978457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd0efba761a231895f368b69fcfb841d12e808ff00c5c6f2ac2109b597c4aa0`  
		Last Modified: Sat, 27 Jan 2024 02:53:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a454fea33342d6c0823e4e1cc0264660e8334d28b49a1b9443e4358a14119eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00da2af7b35489a63b9e58861553eda992f815952ce9153808cd75b2093adfd`

```dockerfile
```

-	Layers:
	-	`sha256:88d0965632076c162b2ddce55dfc26071562a77f583a521ba181c6ca232bdbd5`  
		Last Modified: Sat, 27 Jan 2024 02:53:07 GMT  
		Size: 736.5 KB (736514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e788d325d3de568c19a01f02652fa1f1fca3270bb2ff7a7455cf1fc12fea39`  
		Last Modified: Sat, 27 Jan 2024 02:53:06 GMT  
		Size: 33.2 KB (33249 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d54567afdaceea675417e46540b3a40bf82dc41c579d9322e6a5396a08ccf4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136242709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2bfcf03bafa1b43f9deba80b3e81d63c584a21bcc0bda5d9a42f69dfc57831`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 24 Jan 2024 12:05:09 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Wed, 24 Jan 2024 12:05:09 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_VERSION=25.0.1
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 24 Jan 2024 12:05:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
CMD ["sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
VOLUME [/var/lib/docker]
# Wed, 24 Jan 2024 12:05:09 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 24 Jan 2024 12:05:09 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
CMD []
# Wed, 24 Jan 2024 12:05:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 24 Jan 2024 12:05:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd627277f8af1d68caa52e5725c89976aa4c6aca5c14958e83eb2143390ab6f`  
		Last Modified: Sat, 27 Jan 2024 17:51:38 GMT  
		Size: 2.0 MB (2019693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fb61f641eda83263d0ea571074960545636883de036a62c02d9b400bf583b3`  
		Last Modified: Sat, 27 Jan 2024 17:51:37 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f4d3b2720d532db2a6c8d833a3ee9057278971e197f9d252f9f9a8d362517f`  
		Last Modified: Sat, 27 Jan 2024 17:51:38 GMT  
		Size: 15.9 MB (15901603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a66ce1aea6b53903f39cdfabd0705977c7481dc43c7c23fd2c39b38f97d3a53`  
		Last Modified: Sat, 27 Jan 2024 17:51:38 GMT  
		Size: 15.6 MB (15640597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7217a52d7a6c4f86df9b0999ef92ede06b25df6a89c8711c672b468bac13a79b`  
		Last Modified: Sat, 27 Jan 2024 17:51:39 GMT  
		Size: 16.6 MB (16609705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc84f27731b3eae7633fca8b847f9e89fbcaad9c46650936d05dd0f37faf10a`  
		Last Modified: Sat, 27 Jan 2024 17:51:39 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b821417b5de9fb90aaff10591cb6687e5bf302909fa4327fd35ede10979c4a5c`  
		Last Modified: Sat, 27 Jan 2024 17:51:40 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca93320a4606c17271499447bee21b1525d1520e609c1e962376720645a65ea`  
		Last Modified: Sat, 27 Jan 2024 17:51:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6058c4c70ece85fc79ac3e634829ad6d93e42235ff7fc3c58f0ebffda881b4df`  
		Last Modified: Sun, 28 Jan 2024 00:32:33 GMT  
		Size: 7.4 MB (7428526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d19537f3db0836661b5cd00e0d3d500195af8c1b7d08be987d9066ee9867cb`  
		Last Modified: Sun, 28 Jan 2024 00:32:33 GMT  
		Size: 93.1 KB (93074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bba257714a561ef2cbd172ea9d0979ac4bc205ee4266572f5a9f1bd51561a54`  
		Last Modified: Sun, 28 Jan 2024 00:32:33 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68ebae8406e645d09ccc84ec3f99981ed5a0892050b60d258844ea2a2d9a5ab`  
		Last Modified: Sun, 28 Jan 2024 00:32:35 GMT  
		Size: 51.3 MB (51341270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153f727121596c602878c19e1ede66176b65d0ce7e6afb1b89d286e8803890c4`  
		Last Modified: Sun, 28 Jan 2024 00:32:34 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005e355a261ff5ff3193eb39e9eb1b9b5eefcd37f0953c754f8212cd92b37a0c`  
		Last Modified: Sun, 28 Jan 2024 00:32:34 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474e5ea4d413cd1499581591ecfb1607527450da1d084171d6f92fec5d4f831a`  
		Last Modified: Sun, 28 Jan 2024 01:31:02 GMT  
		Size: 1.0 MB (1016241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef476d97b1e50991b2c46f7fdc536bedcac07f9b49ff99ec726e1e4169815854`  
		Last Modified: Sun, 28 Jan 2024 01:31:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa65d848bd2a26baac0f40a79eb2bc0fdcd032fcf065c11fa6ede7fc77ba366`  
		Last Modified: Sun, 28 Jan 2024 01:31:02 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3679f5fd97b82bb57bce21ed1b370fa6cda0b468c97ac35869fc840bfe5a2d6f`  
		Last Modified: Sun, 28 Jan 2024 01:31:03 GMT  
		Size: 22.8 MB (22834334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cb7e538e16f3bea0095603dbdb2f0ed0c902e52bf2f734c94d72422e5654a1`  
		Last Modified: Sun, 28 Jan 2024 01:31:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2814836f5e08a8b2dd8581e3f75b25f6052f63b0d6ef9e5288a239d3081b1937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88b23c48b511aa45b673579eae4898cfa7a7f4c3e562ce19d51017934d25733`

```dockerfile
```

-	Layers:
	-	`sha256:8d7d9c44f6bce773c1c589c5831896dd01ec832eedff348563dde46815402d65`  
		Last Modified: Sun, 28 Jan 2024 01:31:02 GMT  
		Size: 736.5 KB (736525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:119df7969c6e2eac3c5a7794cb336130c519e6e0626afc47134defb659c02db0`  
		Last Modified: Sun, 28 Jan 2024 01:31:02 GMT  
		Size: 33.3 KB (33310 bytes)  
		MIME: application/vnd.in-toto+json

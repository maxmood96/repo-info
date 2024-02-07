## `docker:dind-rootless`

```console
$ docker pull docker@sha256:0c2a80e08e0608c1e66b3435251fb1beac9a3d24c25bdaf64902c5b6e85e8203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:14bab35eb2f9d823bb26a7579484b7c2937a6387e6c71a8f17984c271e5958f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142478267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df6c44ce22ec266cc4b2fb5b274468075df213c1d883c6065af82acfe45c26a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 01 Feb 2024 06:04:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
ENV DOCKER_VERSION=25.0.2
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.5
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-x86_64'; 			sha256='94355be1d1d395040bbda1490f98d5c7627c30798a7955e1f2a78fda33a4b3e1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-armv6'; 			sha256='bd402cf44fec9640c29e85184ddd36c9d4094045b296e2833533d53715d0cfc2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-armv7'; 			sha256='80248b4c2c407b22b24896ff6d6e766be7ca97239c5b8137f47c81b62a1befb4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-aarch64'; 			sha256='535e90ff9a7f24384f8a38f9f9ad49125485af7ae5ffda7226d091e5b8126948'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-ppc64le'; 			sha256='2143fd5df30c29e22869e5461afac0ca1f2b8d435c544b89fc1d826eb9e52df8'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-riscv64'; 			sha256='e4534c48b1bdf68d664ccc426800b215d3708f3a492d57e36b0a412f4d229546'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-s390x'; 			sha256='7def69d38989d1020c49ab37bb68ab2c29558484e33fc952b5258c84cb1bbda1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Feb 2024 06:04:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 06:04:26 GMT
CMD ["sh"]
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Feb 2024 06:04:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 01 Feb 2024 06:04:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Feb 2024 06:04:26 GMT
CMD []
# Thu, 01 Feb 2024 06:04:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 01 Feb 2024 06:04:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Feb 2024 06:04:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d339c902f7d76917f54985966131501fd11a25559762adff7275666ad750e295`  
		Last Modified: Thu, 01 Feb 2024 18:58:05 GMT  
		Size: 2.0 MB (2018464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6da5881d23400be91f76c66fa158878376ddadc8092ac43cd9fc788aad141e`  
		Last Modified: Thu, 01 Feb 2024 18:58:04 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6168663bbb0ae2a9f1a9704bfa7cdacac55433b1e8631328867a17244bc666d`  
		Last Modified: Thu, 01 Feb 2024 18:58:05 GMT  
		Size: 16.9 MB (16894260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54bc4c52de5cd0d13b71e2b1717852501f664d523bbe2a1b9d8c0ecff365624`  
		Last Modified: Thu, 01 Feb 2024 18:58:05 GMT  
		Size: 17.2 MB (17195310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48a81fca6fc57f6bf47f0e7c3e4c0a8be2f25cd562b4a5cef90d2165bc57701`  
		Last Modified: Thu, 01 Feb 2024 18:58:06 GMT  
		Size: 18.2 MB (18195610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f4b43f6a86af4e78ac5674307f9453e05cb7095dd1f303f67a1c01f988c5e1`  
		Last Modified: Thu, 01 Feb 2024 18:58:06 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241e19d5bb55e813177832b0c5cacbe11121425b82f9711b266abea2c793cfe3`  
		Last Modified: Thu, 01 Feb 2024 18:58:07 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18d6143d160d9220d446e915dd6fead256d9f28608917d182644f3c6474e100`  
		Last Modified: Thu, 01 Feb 2024 18:58:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faef9d990511b252cd2785273a16d5abecedce46f627e1b8635f7ed0aa01fe11`  
		Last Modified: Thu, 01 Feb 2024 19:56:54 GMT  
		Size: 7.1 MB (7068082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b031a68dd1131ad731d6c79630b223a7d3d741d687ca26193c714bc4febd62d`  
		Last Modified: Thu, 01 Feb 2024 19:56:54 GMT  
		Size: 83.6 KB (83648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8921a83f1d31a536bf78b45436d0cadd5cfdd2a56958a82c7966aa094b4e2b8a`  
		Last Modified: Thu, 01 Feb 2024 19:56:54 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6bae68ae7274d984f9d5e111c19bcb72d56cc7359f09057b518318ae5489c4`  
		Last Modified: Thu, 01 Feb 2024 19:56:55 GMT  
		Size: 55.7 MB (55651670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3701828773b1739bd502bb852cfc28c9b9ae88d96b78697f2d536a63cc29a91f`  
		Last Modified: Thu, 01 Feb 2024 19:56:55 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f810b3a3d2303285e785b87ed3a8d2bc904f9bb603e7668b03ef9d6024f1e758`  
		Last Modified: Thu, 01 Feb 2024 19:56:55 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd97824ac15d0f86ba0d543f57b0f46a4718855a082906f3076374fa33affc8`  
		Last Modified: Thu, 01 Feb 2024 20:56:42 GMT  
		Size: 974.0 KB (974048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4b85c67b3eade13c85ca8750623647f5b1d4404933d4392b04c9d2f8da90b0`  
		Last Modified: Thu, 01 Feb 2024 20:56:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68abc640258c8628266fb2f184c987fd4cacc27b18dcab0fe12e1f9d2bc38822`  
		Last Modified: Thu, 01 Feb 2024 20:56:42 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf204a05084cdf47b50ad3f3f2f4f402d7319adf2d3d4926d39cc2f2a801c48`  
		Last Modified: Thu, 01 Feb 2024 20:56:42 GMT  
		Size: 21.0 MB (20978489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c59ae4305108667af8785185b656223d5e67be5022a29b493ca6e8613abd61`  
		Last Modified: Thu, 01 Feb 2024 20:56:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e51d5346dff6cd071667c2d49910c4f27e80f2f8e85e132d45a9255a7a199146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.3 KB (769263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc08eb2728fd451ecc3c47a7b1f9e37e0960b038f45dfe0a53ba922fb692235`

```dockerfile
```

-	Layers:
	-	`sha256:e730fefc67c5f4d68cb5d6f77f67c44d0d9864ad96c0e81de1d02ef9410c2ff2`  
		Last Modified: Thu, 01 Feb 2024 20:56:41 GMT  
		Size: 736.0 KB (736014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7032a415ab9ca1cb3b4c671cb24cb1e483016fdaf3968aa7b3170ade539da8e`  
		Last Modified: Thu, 01 Feb 2024 20:56:41 GMT  
		Size: 33.2 KB (33249 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f3ff5c727583f3e7897e95a08d9fe352019632dba7e7f62462cc88562f53687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136267419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebde2542991685e83488b999375e589064e32928f3f7183430fc958fbd24bba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 00:56:51 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENV DOCKER_VERSION=25.0.3
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.5
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-x86_64'; 			sha256='94355be1d1d395040bbda1490f98d5c7627c30798a7955e1f2a78fda33a4b3e1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-armv6'; 			sha256='bd402cf44fec9640c29e85184ddd36c9d4094045b296e2833533d53715d0cfc2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-armv7'; 			sha256='80248b4c2c407b22b24896ff6d6e766be7ca97239c5b8137f47c81b62a1befb4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-aarch64'; 			sha256='535e90ff9a7f24384f8a38f9f9ad49125485af7ae5ffda7226d091e5b8126948'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-ppc64le'; 			sha256='2143fd5df30c29e22869e5461afac0ca1f2b8d435c544b89fc1d826eb9e52df8'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-riscv64'; 			sha256='e4534c48b1bdf68d664ccc426800b215d3708f3a492d57e36b0a412f4d229546'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-s390x'; 			sha256='7def69d38989d1020c49ab37bb68ab2c29558484e33fc952b5258c84cb1bbda1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 07 Feb 2024 00:56:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 00:56:51 GMT
CMD ["sh"]
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
VOLUME [/var/lib/docker]
# Wed, 07 Feb 2024 00:56:51 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 07 Feb 2024 00:56:51 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 07 Feb 2024 00:56:51 GMT
CMD []
# Wed, 07 Feb 2024 00:56:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 07 Feb 2024 00:56:51 GMT
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
	-	`sha256:733caa8798619f3c785aab636db1c660bf8ceee8e77ed49cf3970f3f30c48be2`  
		Last Modified: Wed, 07 Feb 2024 02:22:59 GMT  
		Size: 15.9 MB (15902172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b482f87146141bc3e2bedcc4a540b3bbb60ce0e2066e192b06baa1aaa64e28`  
		Last Modified: Wed, 07 Feb 2024 02:22:59 GMT  
		Size: 15.6 MB (15640606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f596b0f1ebd661fd094886e266477d7f0a587513e711e4983b7b1a109ed9d72`  
		Last Modified: Wed, 07 Feb 2024 02:22:59 GMT  
		Size: 16.6 MB (16619376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c18ba07c5247d502d4d6158f8dc0b29d0a4ca0bafc3d33084469876f3e8bded`  
		Last Modified: Wed, 07 Feb 2024 02:22:58 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5136b0c9c408a7218063243499b86e3cec20c8071872d7c076290fcdfb2d663`  
		Last Modified: Wed, 07 Feb 2024 02:22:59 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66fedb273ac8d47f734d08b2122917564cfd3396f8316110969bf858c0feba2`  
		Last Modified: Wed, 07 Feb 2024 02:23:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b4790c78e16f93dda05c8063e0f5f27a283df16c15c10d0fd6896eff0fa484`  
		Last Modified: Wed, 07 Feb 2024 03:27:08 GMT  
		Size: 7.4 MB (7428529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778c48064a9e18a6a0b8ab4ae653a3d0841eb45b892161843b18a71eac11f8a4`  
		Last Modified: Wed, 07 Feb 2024 03:27:08 GMT  
		Size: 93.1 KB (93076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf1811cd93b31e92291d87cac27b8f42bc8c993bd004cf1b89df6b65373de44`  
		Last Modified: Wed, 07 Feb 2024 03:27:08 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097af4b233d2fbd272c5737630e6866bfd18e90f68ef5efe9185cc36fed69cc`  
		Last Modified: Wed, 07 Feb 2024 03:27:10 GMT  
		Size: 51.4 MB (51355073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efeff7477ffc5e1fc8970e747bd02aa25a404f4244eee2cb4904cf39b00c1e4`  
		Last Modified: Wed, 07 Feb 2024 03:27:09 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295ea359eb0b75ea072b917e03da98bb6b01bb0008bc9c4f1c9c1a90931831fb`  
		Last Modified: Wed, 07 Feb 2024 03:27:09 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925d0483d3bd54d227098452133c5c6b61937cbaf74139b666dcb9ee9091aacf`  
		Last Modified: Wed, 07 Feb 2024 04:23:48 GMT  
		Size: 1.0 MB (1016242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141be1fab09cb44d105eddd7182e86f7c70b9d2348d7c73e188709120a4e3308`  
		Last Modified: Wed, 07 Feb 2024 04:23:48 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b711d7049e498bf3a14ae07da58fe624901e9176fbbdda3206e984823623e44f`  
		Last Modified: Wed, 07 Feb 2024 04:23:48 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe450770b5960672c2ae0c1ace25fe697db9bf96bf1fd82fa80161dc782f447c`  
		Last Modified: Wed, 07 Feb 2024 04:23:49 GMT  
		Size: 22.8 MB (22834977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43086a7421a580be210adc2cd5fa6fbf5d1872bda12557b4c3dc3b745ea59a8b`  
		Last Modified: Wed, 07 Feb 2024 04:23:49 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:eef576f5786bb86c77112ea64caf407db52d4022b36f28291d64b4a6e41610bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.3 KB (777270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d63f09756ed0b0b63a9eadb600122421bb50dc2a7d946d05f78a22211bc3988`

```dockerfile
```

-	Layers:
	-	`sha256:24d9c91d9b629f1c01e6e738eb5a732024fdbb7b955015fb22b9122bef0b6a96`  
		Last Modified: Wed, 07 Feb 2024 04:23:47 GMT  
		Size: 744.0 KB (743958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c3ad9e4add47c9c2aa7c24bc1b93c6a591d19b82185a2b7c7c46d90ef7ffd4`  
		Last Modified: Wed, 07 Feb 2024 04:23:47 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json

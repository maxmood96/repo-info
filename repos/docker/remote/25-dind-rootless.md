## `docker:25-dind-rootless`

```console
$ docker pull docker@sha256:ae8ce8bc7f6328cf60484a821769addc484c165d4f86a408acc7051f792e949b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:25-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:85d09f5f026b384dfcc1321eace4ead7ce84b031101755bbcf849ac3bb3bfbd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147594261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6286f71320206633133c81e73079a11606097def598f1cca96cff0d101687ec4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a25a43dc0fd6c136362b4a3d6db775c9ef70c9a174c9fbc3e289e68666700f9`  
		Last Modified: Fri, 16 Feb 2024 19:51:01 GMT  
		Size: 2.0 MB (2018470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8453b14f8be15bf6f299681f30d380496a111db88c351a8ddb1197d367126462`  
		Last Modified: Fri, 16 Feb 2024 19:51:00 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5449a857d65674331676d8a0ae1f1f61d96270c2ee31563e38bb9f2dee2d4e9`  
		Last Modified: Fri, 16 Feb 2024 19:51:01 GMT  
		Size: 16.9 MB (16894488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dde2c9dd2648770569cff7c0361f355f18793dfe4bd84d1fba979943ee74855`  
		Last Modified: Fri, 16 Feb 2024 19:51:02 GMT  
		Size: 17.2 MB (17195310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b786ed2257177c2b9aa6ccfdd0c99c8c712f2bd78c2c0ce6f6639f18bd1e8c`  
		Last Modified: Fri, 16 Feb 2024 19:51:02 GMT  
		Size: 18.2 MB (18208514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fa2b1e15e27754d53ffaf67b70bd3a96c83991288565c31dd7e8d90576feaa`  
		Last Modified: Fri, 16 Feb 2024 19:51:02 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b17757db9c4144873b7337f801d9baf94791cf43fa4d9db25f4cfb4e186da5f`  
		Last Modified: Fri, 16 Feb 2024 19:51:02 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8480c0a982cae1130a3fcc627ede9d7df453984e0406e7e46b44437812a620`  
		Last Modified: Fri, 16 Feb 2024 19:51:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97024fa66b691923ec043077c4c91a83076bcd36aa584b122be6ae5ee33951a0`  
		Last Modified: Tue, 27 Feb 2024 21:51:34 GMT  
		Size: 12.2 MB (12156155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c9909845b0a81d54e130d908e7cb61a776075336a2aa2b161aa9a07a146cde`  
		Last Modified: Tue, 27 Feb 2024 21:51:34 GMT  
		Size: 88.9 KB (88864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab157ace34a1a24a7835644fe6904ba42d3b9bc5cadacb8a9b5dedf9f3d7a089`  
		Last Modified: Tue, 27 Feb 2024 21:51:34 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f5802f12dfd684e65e6345c89bb460dee58268965304f6670829f65ab32f8`  
		Last Modified: Tue, 27 Feb 2024 21:51:35 GMT  
		Size: 55.7 MB (55653334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f3ade57aa7993e47effac8b4fcb0e1f8611cb0a23f6cef4341511a21523291`  
		Last Modified: Tue, 27 Feb 2024 21:51:35 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a8e9699976d483904318fbcbf847c3cb6ad64980e8a97842cf25f77a4ebc5c`  
		Last Modified: Tue, 27 Feb 2024 21:51:35 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096d00c74587ac4fca088e7b6e4bf9e30d7a358ffdb4e8c13a41ef232d6c9dc3`  
		Last Modified: Tue, 27 Feb 2024 22:50:24 GMT  
		Size: 981.3 KB (981311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c005594f48173715c9794bcfe69c967e8b661b2dd2820eec6ec49b4b219bcf`  
		Last Modified: Tue, 27 Feb 2024 22:50:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd42382fbb4a9fa465ca66b88a6a09e67f44e94299ecdbb3285012b44d4d672`  
		Last Modified: Tue, 27 Feb 2024 22:50:25 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4658fc621bbf7dcae2462c98206388f800ecce11ce58bcef33b38c733c502c2`  
		Last Modified: Tue, 27 Feb 2024 22:50:24 GMT  
		Size: 21.0 MB (20979126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66251814ea55809fde150d68f2bed9d5c68660fdc899d90772a111a7dc5c4212`  
		Last Modified: Tue, 27 Feb 2024 22:50:24 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f3ea43d89174e5b154e1d31d47633ad83008241999b71a77c559c4fade001973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.7 KB (905744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdb443e2eb5bd8b86aef432072125a6517740f3f52e001e134a4cf33f4d3af5`

```dockerfile
```

-	Layers:
	-	`sha256:dac4f233c5a50b3d6d8c6baebe6ad53f7c111757c1b3fcfc51e51b11533e42e9`  
		Last Modified: Tue, 27 Feb 2024 22:50:23 GMT  
		Size: 872.5 KB (872488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eda827886d34997f80f0b20a54df3bacff6ac03fe07a17e022f5b1024c09d5ed`  
		Last Modified: Tue, 27 Feb 2024 22:50:23 GMT  
		Size: 33.3 KB (33256 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4992211b7f56b44a9ec73764e675e7c58fe2aebfb95917e04f2e5511319d460e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141498290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16d26be8d0919df83b92454f5cd6a275e424cafd5943468b0a404215a949349`
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
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
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
	-	`sha256:1ffd3afa1d3effdddb0b7e31a7cd39e3e94cd96bdc4a5ed48e796be9f66324f6`  
		Last Modified: Fri, 16 Feb 2024 20:28:15 GMT  
		Size: 16.6 MB (16640439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d13b96e2ce43240c9c9186b956f883e140b17694a75dc291ed5d6564282441`  
		Last Modified: Fri, 16 Feb 2024 20:28:14 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872b0ec9e92a0ff66e85293db6870897cccf3d0277ac9bfe3d3af60841cd7f3a`  
		Last Modified: Fri, 16 Feb 2024 20:28:14 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a41040cfda23c170d5a25b35ca4f9ccdab85d729c61312cc7e1be223b27bb32`  
		Last Modified: Fri, 16 Feb 2024 20:28:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12b5842cd88fe780f03562a537937f35d2e947c097335c95930973e40d09b63`  
		Last Modified: Tue, 27 Feb 2024 22:17:11 GMT  
		Size: 12.6 MB (12626808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fed680ddf104d1ef2eadf0004d63deb0a457f0ed8576f5e85a8ea4eed41ac7`  
		Last Modified: Tue, 27 Feb 2024 22:17:10 GMT  
		Size: 98.4 KB (98376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f799a7b288ef62f942732f0105e9ffaecb4f8237e75f6a9b37677ea506ba88`  
		Last Modified: Tue, 27 Feb 2024 22:17:10 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b711c26ad6148d3481de6d5410dc876f1323572fa12cf726c78694c1e2dec4a8`  
		Last Modified: Tue, 27 Feb 2024 22:17:12 GMT  
		Size: 51.4 MB (51355055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce59fe0e7942c27952508f6c230946c013a4fbd9fc38cd49f80db7ee631dcae`  
		Last Modified: Tue, 27 Feb 2024 22:17:11 GMT  
		Size: 1.5 KB (1507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c26fbe85d26b0157fd68ad78ac224e507b8d6bfbd9211312f287ebaefc86971`  
		Last Modified: Tue, 27 Feb 2024 22:17:11 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b793455d1d20bf712b0fa28f6fbb855c717d341be45ef57a0a483b6161705f`  
		Last Modified: Tue, 27 Feb 2024 22:58:24 GMT  
		Size: 1.0 MB (1022480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5925033c44f541841f34349a1de8c4bb3dc0b255c80b705e8948354d71e7cf`  
		Last Modified: Tue, 27 Feb 2024 22:58:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a0b37bc01627352479dba0c47b3df6cbc2e8f7d4b1bc769cfd2fa6989175eb`  
		Last Modified: Tue, 27 Feb 2024 22:58:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89caefe18b443d99e3ffc1227439a2e23679c66f7dc35533a449e1e6953ff42d`  
		Last Modified: Tue, 27 Feb 2024 22:58:25 GMT  
		Size: 22.8 MB (22834981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeecc04f1ac663e613349967ff5b14b96b11dcbe2f4e7720c222d235b0a3777`  
		Last Modified: Tue, 27 Feb 2024 22:58:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1798540903c74fc565e808024eb6a0e602acdd0a25f030e009a3df7e8ca3f8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.8 KB (905818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9f9257f5047652ba45a9c70b555b55b23b3e2a5e6e0f8cf46ef3164a43f0b2`

```dockerfile
```

-	Layers:
	-	`sha256:cc4a4abf673d51c91458909ae23b992d7fed26ae8889bd9c0c791e9caa897c27`  
		Last Modified: Tue, 27 Feb 2024 22:58:23 GMT  
		Size: 872.5 KB (872499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30b308a9b94354b551622418d35d6cb7505f82e86ec7894179db99ec451cc69`  
		Last Modified: Tue, 27 Feb 2024 22:58:23 GMT  
		Size: 33.3 KB (33319 bytes)  
		MIME: application/vnd.in-toto+json

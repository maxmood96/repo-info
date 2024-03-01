## `docker:26-rc-dind-rootless`

```console
$ docker pull docker@sha256:28ae65cb19fca9fbf0b91c590b69e42eb76cd928565e2cfec85e5fb0fad605f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:26-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:1aba10b4e32344282b19f4f21680d0616606e0787576754af9ad54b70fcc741b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148295001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd98c507e3d7c0f90932ed23b4de028984a641cfa08d1341eb4cbd90a9603139`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD ["sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
VOLUME [/var/lib/docker]
# Thu, 29 Feb 2024 11:10:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD []
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 29 Feb 2024 11:10:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238a0291d2775c9c58a81d97c0a6ee6d7456f9dcfb53274d8394c29d8f32ef1b`  
		Last Modified: Thu, 29 Feb 2024 19:49:02 GMT  
		Size: 2.0 MB (2018448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0a6a69c9223cbeac96a98d829b7defd1198309e4c39e7530ee337d4889b1f0`  
		Last Modified: Thu, 29 Feb 2024 19:49:02 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a8e00b723ec9b1c002c2dddb8a264ad57cb559d35a37668e764d7e88e274b2`  
		Last Modified: Thu, 29 Feb 2024 19:49:02 GMT  
		Size: 16.9 MB (16906057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ad9dfe6dcd75b86ed5b9ddd8d9766723fc222fd596bbbf3f1d56c777c7dbcc`  
		Last Modified: Thu, 29 Feb 2024 19:49:02 GMT  
		Size: 17.2 MB (17195299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680582dd5f6748caca89d3f4149ae100db56f6466396ccdf32ece2546deddb37`  
		Last Modified: Thu, 29 Feb 2024 19:49:03 GMT  
		Size: 18.2 MB (18208514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5339634a3f121e1cb897e888209eeedd655a8fec1645dead6162d5f619fd27`  
		Last Modified: Thu, 29 Feb 2024 19:49:03 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3966f289c893f3596bba3677432bb6c2a4cf1f2fa9983ac4d1a940ce9089d498`  
		Last Modified: Thu, 29 Feb 2024 19:49:03 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af99726b899005908fad4b410e2d949e6fc4beec7aba1a3105662e60d30765c9`  
		Last Modified: Thu, 29 Feb 2024 19:49:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d202d6bf3867ca80b441dbebcb065fda430287b344a392606fa7dd449c284fc`  
		Last Modified: Thu, 29 Feb 2024 20:48:42 GMT  
		Size: 12.2 MB (12156195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c83ed4c6a6f5050778f0ee2fa27118983d1b8e21785ee2e2a840ae5f807bdb`  
		Last Modified: Thu, 29 Feb 2024 20:48:42 GMT  
		Size: 88.9 KB (88862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd47167ce19d7ea088c416571dc4e4b4da090218b9fb473854cc0df86216e980`  
		Last Modified: Thu, 29 Feb 2024 20:48:42 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805ea23394055c895f2f0719aeba8c241d6ad5f4e0098db898891e966142bc05`  
		Last Modified: Thu, 29 Feb 2024 20:48:43 GMT  
		Size: 56.3 MB (56346603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8233c911483365dd64e6f346086325094bde5c25d2dff45f24861a00a0504960`  
		Last Modified: Thu, 29 Feb 2024 20:48:43 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3ab0c7de3c11f02db7d38fe5b0668294d32837354076a53384ce6a8746cb29`  
		Last Modified: Thu, 29 Feb 2024 20:48:43 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb14a9829cd5b7e0b1fbdb1494c19697dd66e8bd1fd9baaff8018c08d186a2f1`  
		Last Modified: Thu, 29 Feb 2024 21:48:30 GMT  
		Size: 981.3 KB (981312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8a9d9d67649f09b3e9ff34bcf28438311234db6ca6786c307ebbd077080374`  
		Last Modified: Thu, 29 Feb 2024 21:48:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356163f1f3c5d0428a18134b8f6b37ac206aa3bfb96841af2925d4b981240085`  
		Last Modified: Thu, 29 Feb 2024 21:48:30 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddf87190d28cdb6459a58b1f1fab7b531b6438d2bc730e72de43ac105080f48`  
		Last Modified: Thu, 29 Feb 2024 21:48:31 GMT  
		Size: 21.0 MB (20975024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0867676687d7d04d75cea8682c6f3196dca780dd50af649552114d9bfdcd6b65`  
		Last Modified: Thu, 29 Feb 2024 21:48:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d1463b56c0e714d97674e7a074b557bd45e359ef378a5aa8c9ae71f9f892a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.2 KB (923185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34bf1eeb081ffaf80708a4095408c61cb86a80b738089c061efec592e6798c6`

```dockerfile
```

-	Layers:
	-	`sha256:f5ff9b7accde0fa7824d9dcd553b1742addb337af1d4bbff64808940a73c2c5e`  
		Last Modified: Thu, 29 Feb 2024 21:48:29 GMT  
		Size: 890.2 KB (890191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fd370ab2619d4749e30fce8394faf394deecc3bdaf2c8ed61a3a8971796da5`  
		Last Modified: Thu, 29 Feb 2024 21:48:29 GMT  
		Size: 33.0 KB (32994 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ed70ddc53127ef7d74478750a4adba5a8b9b6da263f2ee3006c63dc60d0ae393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142150352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36d32e2c362d5a54ce841d8b7a606c579e69aeeb97baf48943f8316fcf05784`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD ["sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
VOLUME [/var/lib/docker]
# Thu, 29 Feb 2024 11:10:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD []
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 29 Feb 2024 11:10:50 GMT
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
	-	`sha256:d5e373947c633ebf3fa9986ae70a2fd71f8df3215c7243e45124c067fd4548fc`  
		Last Modified: Thu, 29 Feb 2024 20:00:13 GMT  
		Size: 15.9 MB (15917020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175757f58356331e958899b4d5e45a3f2b639ddec46c4cae57a44741ac538201`  
		Last Modified: Thu, 29 Feb 2024 20:00:13 GMT  
		Size: 15.6 MB (15640596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657ac24788fe05605b760abd9d5b9b1fc663c92de3870c60805b00c0e29709e8`  
		Last Modified: Thu, 29 Feb 2024 20:00:13 GMT  
		Size: 16.6 MB (16640489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68660a4b8ae70fc6a495d7eeb9dfa4fe01328afae2cd6d9fc914c73c48ecb5da`  
		Last Modified: Thu, 29 Feb 2024 20:00:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838e1329e0d77349ff18111bf4a7f447953856f6fa0417674c5ff064a513d830`  
		Last Modified: Thu, 29 Feb 2024 20:00:14 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3860585275b2dc666f25566e11b743ea4e441382777b0b808df04ffb5599111`  
		Last Modified: Thu, 29 Feb 2024 20:00:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1bfcd5098982cbf462e44f5c8e0c4352c15ef8c6bf730fde90c8ce7cb67d70`  
		Last Modified: Thu, 29 Feb 2024 20:51:51 GMT  
		Size: 12.6 MB (12626950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846b2cd1cbd504fa292b54bd3e71a12de4de612779273a7c00a40f5442f1d805`  
		Last Modified: Thu, 29 Feb 2024 20:51:51 GMT  
		Size: 98.4 KB (98380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38228a0e69eeaae700099f9d0baf37de2d6d74af7a0af4695c5786bf405d3422`  
		Last Modified: Thu, 29 Feb 2024 20:51:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9aa3532f63c4d2696e64022bbb719f51bc72600935ef12dc5b4831fe970e92`  
		Last Modified: Thu, 29 Feb 2024 20:51:53 GMT  
		Size: 52.0 MB (51991143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79491999133f06d5a6f297ae143f1f04bb8fa4a172fcc315e382762916f138cc`  
		Last Modified: Thu, 29 Feb 2024 20:51:52 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9e04ede7ff56ddc7a1ef7ea99408a6990935fb92c45e630518fafd09817b3`  
		Last Modified: Thu, 29 Feb 2024 20:51:52 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a214e8201d891d391bbcb27271023a864c6b9e19509104c2eb23421fc0b908e9`  
		Last Modified: Thu, 29 Feb 2024 21:51:25 GMT  
		Size: 1.0 MB (1022484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527bdad640253616209795b96bc5107284daf67bc60649f4de1602611ed23e4c`  
		Last Modified: Thu, 29 Feb 2024 21:51:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9664cbc703840d12f569a67e25e3ef07c71cee5f7ec8a81193bc5f32e009a4dd`  
		Last Modified: Thu, 29 Feb 2024 21:51:25 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11020a95d9e85b79e9cd9da860775a58809718fa697ed7c3fc88c9bc2e146b0a`  
		Last Modified: Thu, 29 Feb 2024 21:51:26 GMT  
		Size: 22.8 MB (22835927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d423be4e0add4d69a6b38a77ae1fd57bab68141acb68ff6191297ee910098f6`  
		Last Modified: Thu, 29 Feb 2024 21:51:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d2e66acddeba45495e892f462527316e32d5500deafb14808a1c86313ccecaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.3 KB (923255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490a15fe5af617574411c2d773c08d748349604dfe35a6c15ff0411ac1a3249b`

```dockerfile
```

-	Layers:
	-	`sha256:fcf03dc2f7f5e25971465e75c93dc62ce3a14adb865f95e5df31a49b25052ec2`  
		Last Modified: Thu, 29 Feb 2024 21:51:24 GMT  
		Size: 890.2 KB (890200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec6fc8529b3d23294f708e4a525ae280463e09693ca9e1a47e35bc6d44835fe`  
		Last Modified: Thu, 29 Feb 2024 21:51:24 GMT  
		Size: 33.1 KB (33055 bytes)  
		MIME: application/vnd.in-toto+json

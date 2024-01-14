## `docker:dind`

```console
$ docker pull docker@sha256:d427455a328e3d7c8a612f4953336b1efe60343f3e17d557831fb4a3581950a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:63897b20cb7da770f94301070dafc902f43cacee189c71c15f6a21e7caeecda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120917406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f38e048d9b01e2d287eb7776d7574ff3e20895757dc23c1f586b47d500be50`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-x86_64'; 			sha256='43fb39c0bc24ac796123935032eddcfb57a7acd9216badeb10714c986ea1e090'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv6'; 			sha256='cb407cfd396892cc0317ef48570492d7e59445a9f50e92181fdf637548801d55'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv7'; 			sha256='936b474e24a51a51fd797bd18290da6abf72d62a614d8730a1fed3deae816ed5'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-aarch64'; 			sha256='d23d03be5880a2f6555932c572ddbc87bd0e1c4c1985933b7488d948eb2494ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-ppc64le'; 			sha256='f52678e23b143b26c2ee20af4ac105ed571bb2e8e39d59478e04bd2d81cbe27c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-riscv64'; 			sha256='555a373414675ae21cafff8280346c94561457f4be254b5576b22f4b5e8f2ab2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-s390x'; 			sha256='37871d879aa0a73f2ac59dab9805bee751d25208bbe72d7d2ab45956f2e1750a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jan 2024 19:06:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
CMD ["sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jan 2024 19:06:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jan 2024 19:06:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
CMD []
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f536948fca5a3c64ac8b2cf66cbe567b30ebaea8b7da79c72c886fb5e1c3786`  
		Last Modified: Sat, 13 Jan 2024 01:56:02 GMT  
		Size: 2.0 MB (2018456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a951c0a4c6359eb08155bc89f362f3aa5ceb06f0c6c1f1f2126a929b9cf9a989`  
		Last Modified: Sat, 13 Jan 2024 01:56:02 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc0aca3ac19dfa2ef201920c022778ffbe3fe3bdcdc5688fd46f993c0f098c`  
		Last Modified: Sat, 13 Jan 2024 01:56:03 GMT  
		Size: 16.4 MB (16400380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037870e22fcd649a33a8ffdafa5abaaaca020930fdcb40c14df4f664739bb061`  
		Last Modified: Sat, 13 Jan 2024 01:56:03 GMT  
		Size: 17.2 MB (17195294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1dee49a0d843723602e95d1cea09ef1926ec9a925d4ab72d2d7dd61a42dfa2`  
		Last Modified: Sat, 13 Jan 2024 01:56:04 GMT  
		Size: 18.2 MB (18172980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f634f72e9c7371b09bb485b5bd71f1b92e043414cec1b047e65209b8ba71a`  
		Last Modified: Sat, 13 Jan 2024 01:56:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90ecee04335aac134164a98cbbd21328e643684560cb5f079319eb5454a3eeb`  
		Last Modified: Sat, 13 Jan 2024 01:56:04 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5ce8279e1cec453677e27b9be35d295f564fd3a9c5f818f0c2cdf48443c590`  
		Last Modified: Sat, 13 Jan 2024 01:56:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa04f136308d216409122312630c5de6f4448201aaa98ba6f8215beb9b0fda3f`  
		Last Modified: Sat, 13 Jan 2024 02:48:14 GMT  
		Size: 9.3 MB (9258205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8386b26d2a0c5e77cd263c54d1750150ae5d654d08b621a8fe6ab38887e928b4`  
		Last Modified: Sat, 13 Jan 2024 02:48:14 GMT  
		Size: 83.6 KB (83647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff805e648bd91fba5e3afc5a0810dfaedb41e49055f870aabc1627cf4b4e6b5`  
		Last Modified: Sat, 13 Jan 2024 02:48:14 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b5e7e6ffb49a9f1dad31b185b91e00b578e8419a716e6f57e585e8e3165aa4`  
		Last Modified: Sat, 13 Jan 2024 02:48:15 GMT  
		Size: 54.4 MB (54371642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60147ed73cd39f6fcbf700aa0e67c12c09986e35896fea581a520fd5c63e6de3`  
		Last Modified: Sat, 13 Jan 2024 02:48:15 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e4a47bb57cdda3b9f24be368c965e2d77804a424c19a5cbaf1a04c954e0b9`  
		Last Modified: Sat, 13 Jan 2024 02:48:15 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:feb9f50a20298d0fa598b27ea047a739d45bc002b1d02e0a85fd8cded54ba0e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.2 KB (738169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc2ea8eece4a4ed1c40d228099f3e83dafdfbb13097a809dd4d2445758f7f19`

```dockerfile
```

-	Layers:
	-	`sha256:cbe4924904cbb3a06a47ac6784009db9b96d61f6928cd7578ea781b03f609d27`  
		Last Modified: Sat, 13 Jan 2024 02:48:14 GMT  
		Size: 701.2 KB (701186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f963350eb551b60af66b6dc1c2e331906489fac5cce99a80854bc4275844872`  
		Last Modified: Sat, 13 Jan 2024 02:48:14 GMT  
		Size: 37.0 KB (36983 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:3c2f905ed63d32522bc472f5332267c89689521725e5c09a863edc14ee7a6f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111791093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1542b37b40f6cae968c90b8350bdacc076cc767e3a848f423fb3ac1983a272c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 21:41:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 21 Dec 2023 21:41:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 Dec 2023 21:41:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 21 Dec 2023 21:41:09 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 21 Dec 2023 21:41:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 Dec 2023 21:41:09 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 21 Dec 2023 21:41:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 Dec 2023 21:41:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 21 Dec 2023 21:41:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 Dec 2023 21:41:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 Dec 2023 21:41:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 21:41:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 Dec 2023 21:41:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 Dec 2023 21:41:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 21:41:09 GMT
CMD ["sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jan 2024 19:06:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jan 2024 19:06:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
CMD []
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc5bd010434069cd814513c40515b0b34d950c4606c108f726b20bc580362b6`  
		Last Modified: Fri, 05 Jan 2024 22:45:12 GMT  
		Size: 2.1 MB (2108662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbc809bdc4cc776e79e9ae1a93a9fed1e6438a007c9fc5f7a92f34cfbaa9fb4`  
		Last Modified: Fri, 05 Jan 2024 22:45:12 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bd0d5d8eb48f81abbfaa7c70409f739d235f25293f0bc2ac09997cac957a27`  
		Last Modified: Sat, 06 Jan 2024 01:47:42 GMT  
		Size: 15.1 MB (15132562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b028388004f00244e4a17457a11711234a2b84e4d33e250284d85c62e53a1fcc`  
		Last Modified: Sat, 06 Jan 2024 01:47:42 GMT  
		Size: 16.1 MB (16099965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ecf1742b110f0f7bd6ccd01419e68921f32aa62478ab255b1da503d6f5866f`  
		Last Modified: Sat, 06 Jan 2024 01:47:42 GMT  
		Size: 16.9 MB (16867519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6af86c77adb225e63b11f16f53ab4aaf8ae0e44a8518c564b07155e4fc8671`  
		Last Modified: Sat, 06 Jan 2024 01:47:41 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722bb4aa882f7e95451704f6190c92b1dba17ad71e37485883863941d3b6177a`  
		Last Modified: Sat, 06 Jan 2024 01:47:42 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b126e325c1b02440c0b9f710295e73e80656036ab2b55c1b74625e8a587729`  
		Last Modified: Sat, 06 Jan 2024 01:47:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ae0da82b0de439e9cb292a440aff71ec0f3657b905bd0f75e1344c91a4b203`  
		Last Modified: Mon, 08 Jan 2024 01:28:32 GMT  
		Size: 7.4 MB (7361988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ce33a02ffbb70f1cdf499e369a140047856db734762a68ba79cd21524ec635`  
		Last Modified: Mon, 08 Jan 2024 01:28:31 GMT  
		Size: 82.6 KB (82597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fa5cee90867babf26b22c3e1bab0163bbb6fe3ff3846e9dfde4afb73a41c51`  
		Last Modified: Mon, 08 Jan 2024 01:28:31 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b04a8ffa95f7862d09c8f9df69abd9c09b4c5741eff2e7dfbdcf61a63a420`  
		Last Modified: Mon, 08 Jan 2024 01:28:33 GMT  
		Size: 51.0 MB (50964337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71f3999c1962e85994b34af1814bde67f415e04fad3600c823b9a38128f24d6`  
		Last Modified: Mon, 08 Jan 2024 01:28:32 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09f387a0359e49c2546adc49c83f7584674a4a03f8a5a4180e1fcf60a58cafe`  
		Last Modified: Tue, 09 Jan 2024 04:06:33 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:f0c8d7fedd4e4f842fec39c24b42ef29e67a5e85f5b7013c128611ba870ca26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 KB (35379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cd475777c69b0106f7b463ed422d4dee744b22d024cdcdf04b6d782d8e4bbc`

```dockerfile
```

-	Layers:
	-	`sha256:f30b9f23e670ac54050c610ff3264297c8f36377be876865512fddb2581d25cf`  
		Last Modified: Tue, 09 Jan 2024 04:06:33 GMT  
		Size: 35.4 KB (35379 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:429be183e14b709beff33769b3e222df08186500aab0d8d1d15f421b186786e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112628631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217de7ecbf8419bb0d7e629cb7ef9036d6c3528c96a6631d64012031931bebe3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-x86_64'; 			sha256='43fb39c0bc24ac796123935032eddcfb57a7acd9216badeb10714c986ea1e090'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv6'; 			sha256='cb407cfd396892cc0317ef48570492d7e59445a9f50e92181fdf637548801d55'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv7'; 			sha256='936b474e24a51a51fd797bd18290da6abf72d62a614d8730a1fed3deae816ed5'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-aarch64'; 			sha256='d23d03be5880a2f6555932c572ddbc87bd0e1c4c1985933b7488d948eb2494ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-ppc64le'; 			sha256='f52678e23b143b26c2ee20af4ac105ed571bb2e8e39d59478e04bd2d81cbe27c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-riscv64'; 			sha256='555a373414675ae21cafff8280346c94561457f4be254b5576b22f4b5e8f2ab2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-s390x'; 			sha256='37871d879aa0a73f2ac59dab9805bee751d25208bbe72d7d2ab45956f2e1750a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jan 2024 19:06:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
CMD ["sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jan 2024 19:06:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jan 2024 19:06:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
CMD []
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f7102b17e4ec828559672f3388bba1ec86d87e7aa09caba4b82fc6870b4fa6`  
		Last Modified: Thu, 14 Dec 2023 22:03:12 GMT  
		Size: 1.9 MB (1888652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f19fa8a6c45d74eb65c7d5844869fef846c8305dd15e21604b2c06e20d1279`  
		Last Modified: Fri, 05 Jan 2024 02:27:22 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a2c3757bdf650079318e50948f607eeba62f86de7a267fdbfb2a7e87d9a101`  
		Last Modified: Fri, 05 Jan 2024 02:28:04 GMT  
		Size: 15.1 MB (15127047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc290c0318cc29f9347ff63de7f0a408796368bc5176069cbf4cfcc75609491`  
		Last Modified: Sat, 13 Jan 2024 21:39:10 GMT  
		Size: 16.1 MB (16084092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef68bce93de44b2bcebe0a6ac7f45d2d7e4ba92dfd45fc2dfec38f4a925afbae`  
		Last Modified: Sat, 13 Jan 2024 21:39:10 GMT  
		Size: 17.2 MB (17162559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f23b963d95078c5f4a22a9f1bc7624fee6611e6d80f054dc3d0c0d23a0eb3`  
		Last Modified: Sat, 13 Jan 2024 21:39:09 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ef4b3c52f4554be0e9f0bdb2430b32b6730cfaa672f1746e9739694b634951`  
		Last Modified: Sat, 13 Jan 2024 21:39:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cae11e72997f437fdffd48fdf3990e6939c4ecc7e988ad1724f9349b580779c`  
		Last Modified: Sat, 13 Jan 2024 21:39:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd95238495af305d28b9b849a10860ec7b089482b166ebad20ed1bec05241cfe`  
		Last Modified: Sat, 13 Jan 2024 22:44:55 GMT  
		Size: 8.4 MB (8396036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bda5c5a1f0dd80ff1511be30d727e7e1025e940d4b961a3c2ccd30501dc4e2`  
		Last Modified: Sat, 13 Jan 2024 22:44:55 GMT  
		Size: 78.9 KB (78892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e34fa2409d2dda90a53a53a18a31ff33034d56fb0b6fa462ee331d0adcee0f`  
		Last Modified: Sat, 13 Jan 2024 22:44:54 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07beb8a71cb864a1b4c7ecb29dec1f7fd0a7041c0bff88f363c1056c05d39f2e`  
		Last Modified: Sat, 13 Jan 2024 22:44:57 GMT  
		Size: 51.0 MB (50964329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb4f6c5fa18d4a210752776c773e363eb6bcff6d3a4b83527736c06f5a54124`  
		Last Modified: Sat, 13 Jan 2024 22:44:55 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d5eb3d7d1261f583c993767ca318419f22db15d931a94c5cec06f6816de87`  
		Last Modified: Sat, 13 Jan 2024 22:44:56 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:525eb9e054ecf0edad785e50d79d8315f534c68557a11de39512a54d545fc625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.5 KB (738477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06793caea74676799f6c8fd90336ed84a8ee509b09d52e001530513e50433676`

```dockerfile
```

-	Layers:
	-	`sha256:33a94e8e23c5ed158432bd1ac4ffad5ae36378d012863557fb69e2c08082796d`  
		Last Modified: Sat, 13 Jan 2024 22:44:54 GMT  
		Size: 701.3 KB (701270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fbe994ea26b53313196977bbecf9d2eec5885addffcc89259d1fb2282547eb8`  
		Last Modified: Sat, 13 Jan 2024 22:44:54 GMT  
		Size: 37.2 KB (37207 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5c9eac105ce4135085975c3b125f3fa14bdff7176ee8f8f0e0b14929f7580864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112383300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f7cd7c4d6c8b2a0e559d9ecf2d210b769cc312532eb3a0f2ff69183c45cefe`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-x86_64'; 			sha256='43fb39c0bc24ac796123935032eddcfb57a7acd9216badeb10714c986ea1e090'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv6'; 			sha256='cb407cfd396892cc0317ef48570492d7e59445a9f50e92181fdf637548801d55'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv7'; 			sha256='936b474e24a51a51fd797bd18290da6abf72d62a614d8730a1fed3deae816ed5'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-aarch64'; 			sha256='d23d03be5880a2f6555932c572ddbc87bd0e1c4c1985933b7488d948eb2494ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-ppc64le'; 			sha256='f52678e23b143b26c2ee20af4ac105ed571bb2e8e39d59478e04bd2d81cbe27c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-riscv64'; 			sha256='555a373414675ae21cafff8280346c94561457f4be254b5576b22f4b5e8f2ab2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-s390x'; 			sha256='37871d879aa0a73f2ac59dab9805bee751d25208bbe72d7d2ab45956f2e1750a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jan 2024 19:06:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
CMD ["sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 04 Jan 2024 19:06:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 19:06:23 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jan 2024 19:06:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jan 2024 19:06:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jan 2024 19:06:23 GMT
CMD []
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
	-	`sha256:904cd2aef7e75dfb117f3229ae16a845ec7fc5a531dc4703c9570b506ea21c29`  
		Last Modified: Fri, 05 Jan 2024 02:15:27 GMT  
		Size: 15.4 MB (15449542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aae6e30004211f7085b9cfa27549866efabba965492a8541247e5bc3339d5aa`  
		Last Modified: Sat, 13 Jan 2024 02:34:42 GMT  
		Size: 15.6 MB (15640596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7ac24ec8f7852a3aac332887ddea5057a34f7aed0c3d6023c7ffc8a7ad197d`  
		Last Modified: Sat, 13 Jan 2024 02:34:42 GMT  
		Size: 16.6 MB (16608020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0426d31fbf2a71b71797f23935ae6fe978003a6a13454a134444035940a7c9`  
		Last Modified: Sat, 13 Jan 2024 02:34:41 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0c5fea991596794d935edf159d493948756548b01987e537275c60223176df`  
		Last Modified: Sat, 13 Jan 2024 02:34:41 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b966bef1de1e839fec89ccdcc17a0bb8e2a601e9ccb4a46c24a167b1cc7337cc`  
		Last Modified: Sat, 13 Jan 2024 02:34:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60b65a77672c4656eb7a2062cedb138cc0884c820355e93b08dc97312f8da4e`  
		Last Modified: Sat, 13 Jan 2024 03:25:33 GMT  
		Size: 9.5 MB (9509852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4762be465b18414f1f88a05b932acaed881b549a4be68ef1a78ccb6b74053e8`  
		Last Modified: Sat, 13 Jan 2024 03:25:32 GMT  
		Size: 93.1 KB (93064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4797a801099c35035070e0d5de9c18b8e868cbbb9b80a63c307cea865291796`  
		Last Modified: Sat, 13 Jan 2024 03:25:32 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bf0765615fccd87c2db4f5e925f17d7e8f61ca086c1297d1031463dc128e8a`  
		Last Modified: Sat, 13 Jan 2024 03:25:34 GMT  
		Size: 49.7 MB (49711211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b42081db5da814f1df305a5acd0982cb4588213bd1fa19a80e436943b978ad`  
		Last Modified: Sat, 13 Jan 2024 03:25:33 GMT  
		Size: 1.5 KB (1507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7445f343f7c2e1b38fad4288c10feb280d06e741ea7d3a4f7d9db71d23b7c0b`  
		Last Modified: Sat, 13 Jan 2024 03:25:33 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:7812356e63efd285f661f3812bc00b633c16f19b5ebfdb3fb8f25716ec63c1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.3 KB (738268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff2e27debdd962d9db8d288be67b3a45ca4db8ff15d557eae1e0cdc367ce705`

```dockerfile
```

-	Layers:
	-	`sha256:8d20c0f449a857937da71ec01ba295c027196c8fbf3f1d81b6d70d8159ec5c07`  
		Last Modified: Sat, 13 Jan 2024 03:25:32 GMT  
		Size: 701.2 KB (701209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e9fc3f86667cbff43e3e9ff98eacced7773acdc13c16cc4cc6e1c28a3c9ce7e`  
		Last Modified: Sat, 13 Jan 2024 03:25:31 GMT  
		Size: 37.1 KB (37059 bytes)  
		MIME: application/vnd.in-toto+json

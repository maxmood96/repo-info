## `docker:24-git`

```console
$ docker pull docker@sha256:e4fa9e5a915e7cc346eb5ebb5325c7d903b0d3428f36319c62751694b4d98b46
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

### `docker:24-git` - linux; amd64

```console
$ docker pull docker@sha256:6a0ee6c795de4b161e644dd4c24e267c623cf55dd2bee7e362468365f50b4674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126049936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5a2b73cfbde479ddcc1abf126296d561fceb28a9675e3e568a7b4f10128cde`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.7
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e576b06aa985d43e76ed4f96d9db258882dfce9764793bf8bdc7919902bdf611`  
		Last Modified: Wed, 24 Jan 2024 20:54:47 GMT  
		Size: 2.0 MB (2018458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee20591903e7a0dae137c80b7d779c1da43b795b56c47fe50f5b9f1fa68f0e66`  
		Last Modified: Wed, 24 Jan 2024 20:54:47 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86ba10d550e1898460cb79c4668574e66bf40fb01baa2fcd6f6c41a28e6c25c`  
		Last Modified: Wed, 24 Jan 2024 20:54:47 GMT  
		Size: 16.4 MB (16400391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbf8e8129baf111e0be9de9431c85fff52a4340dd3f589338aabf2cfd11034d`  
		Last Modified: Wed, 24 Jan 2024 20:54:47 GMT  
		Size: 17.2 MB (17195299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2dee575a196bafa400e71af6828de1754844399e51acb068a3cfa9cd40a09`  
		Last Modified: Wed, 24 Jan 2024 20:54:48 GMT  
		Size: 18.2 MB (18175335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c940c0e24076efba8b3edf240f5aa7609fefe1fe9ee6138fa29a55d7a1ee04`  
		Last Modified: Wed, 24 Jan 2024 20:54:48 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5461273c3c8b419cac9162e836f7868bd65ed259ed3c38b46f3ccd630d0921`  
		Last Modified: Wed, 24 Jan 2024 20:54:48 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b654930f04c2410a3fc811848455a5f7b3d67d3bf80f5239831dc918eabf5b`  
		Last Modified: Wed, 24 Jan 2024 20:54:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79977eb2a13a3406b5c583048251421a4480481fba3286042ce3287cc63c7c81`  
		Last Modified: Wed, 24 Jan 2024 21:49:32 GMT  
		Size: 9.3 MB (9258224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa5a551e89471922bd2d161b2e762702fc83737c3121b16e6438e3e5c58dff1`  
		Last Modified: Wed, 24 Jan 2024 21:49:32 GMT  
		Size: 83.6 KB (83643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0770b9e2ca9ab95dfe13f207f8b885502706f3e851a39d57946f5829ceaa8276`  
		Last Modified: Wed, 24 Jan 2024 21:49:32 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e8fa2ed43292bdde386f122f09f530a42e812ced6add40b8a7b943ebb01de6`  
		Last Modified: Wed, 24 Jan 2024 21:49:33 GMT  
		Size: 54.4 MB (54371626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9e795a98c2fe0d5bd58ab1ec41b3abd85d7d013f931e05dc2fdaf527d2319b`  
		Last Modified: Wed, 24 Jan 2024 21:49:33 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1a2335462b20e7edfb29dc175fd87e333c46527b0ac246a06fb2d4d915dbd4`  
		Last Modified: Wed, 24 Jan 2024 21:49:33 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e0ae698fbec2ce0fe10ccadc281b7590f18bc5a05d925a005b9d5106396ae3`  
		Last Modified: Wed, 24 Jan 2024 22:49:47 GMT  
		Size: 5.1 MB (5130159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:dfff98ef45d5f8184f6ec64138c0ef6ae3127456863940115ba65bec3503eabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.1 KB (760061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44724495c6dc032861fb6f57abe8fc4dd2a0cf3358304722c07790935495f9c`

```dockerfile
```

-	Layers:
	-	`sha256:d2f0a01d5e6667f9f424969f98f72897001da8cc05123e6465134be09a10782c`  
		Last Modified: Wed, 24 Jan 2024 22:49:47 GMT  
		Size: 746.5 KB (746505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4821d6ddd7e371d83c7bdacf92a0980089676546a8943905fb990fa6930c3054`  
		Last Modified: Wed, 24 Jan 2024 22:49:47 GMT  
		Size: 13.6 KB (13556 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:8e8cdc0e136fbbf07a6fdc60a1e11ea6c3ab5c49c32b305f79991290fd834153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119075995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba39ec5b567dc891f08c2146559f5598571028f40d2460fbabdf7a8139ef7d3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.7
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441706b0b6a79717692c9778c5f50078980694f27e12ce415b2197836c0b2121`  
		Last Modified: Tue, 23 Jan 2024 10:53:06 GMT  
		Size: 2.1 MB (2108638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274588671fecad1a12373b82e5dc2aca58048bc38e5d3f037db38ade3324925`  
		Last Modified: Tue, 23 Jan 2024 10:53:05 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481231c19abe20f545e5ceaf5b3e3f1fd2095aceb797b4e183fc22d5b286b391`  
		Last Modified: Tue, 23 Jan 2024 14:02:32 GMT  
		Size: 15.1 MB (15132560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e91ee9b2f5fd16248d7688e402e7ff9ea20caec26239131b78ec923f7060a5`  
		Last Modified: Tue, 23 Jan 2024 14:02:31 GMT  
		Size: 16.1 MB (16099975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20e01c5df880fc346217bdd96a6f8307d53b36f0d12b0776d0063872d1f0cbf`  
		Last Modified: Wed, 24 Jan 2024 21:00:30 GMT  
		Size: 17.2 MB (17174198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1325e4cf7f80b084b8cda5823e7b534317dbefb04693273fac1d74905c6373b7`  
		Last Modified: Wed, 24 Jan 2024 21:00:29 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920baae6a476fffc2e854d1363a59761fe865e7eeb5ea770bed698b645ce0ca`  
		Last Modified: Wed, 24 Jan 2024 21:00:29 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac2d9e943ca1fe86dc7d07ce273d1f9ec6046d0d11de44691c14f96e5d73de0`  
		Last Modified: Wed, 24 Jan 2024 21:00:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bafb9d289d01ae0f244158b3972680e0fd43835cb67414c2f5c8fe9dd59459`  
		Last Modified: Wed, 24 Jan 2024 21:57:18 GMT  
		Size: 9.2 MB (9234233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b07bd0a573c1a66f5b32f8efed6800e6e6513148e67f5e74f5f70ff3dd42c3b`  
		Last Modified: Wed, 24 Jan 2024 21:57:17 GMT  
		Size: 82.6 KB (82598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfad77d92acadf9a96818771ed45c973d99dfd64e3ceb25e8524f831f349f12`  
		Last Modified: Wed, 24 Jan 2024 21:57:17 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e730a8193f75a310110a399ef83ad0871c51ab40c1bb34e9d945171ea22b06b2`  
		Last Modified: Wed, 24 Jan 2024 21:57:19 GMT  
		Size: 51.0 MB (50964360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19905d803308ff748fd7fbe97f99db9bfea7037c48ffb382f85c76a9dbbc0e0`  
		Last Modified: Wed, 24 Jan 2024 21:57:18 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fb581afe8d3c9ed0602afa665e3260c5839d33ed85ba57effc2c30ccb4953a`  
		Last Modified: Wed, 24 Jan 2024 21:57:18 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbc61905cc7a476c79411220f13f462f788eda1ebdfb4299fec38843113beea`  
		Last Modified: Wed, 24 Jan 2024 22:57:25 GMT  
		Size: 5.1 MB (5105964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:78514020266b10253fa1d9e33f623bcbdf977c575b683c3d43c42833d0131098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb19cd012a0fc0a9c7c72f4c9c58f11b7e72ae33bcca0c562f77d479c59e9a`

```dockerfile
```

-	Layers:
	-	`sha256:287ab4058f251ab8e0651b67ec902f16aab0b9b22de65560cff7af875568c8c5`  
		Last Modified: Wed, 24 Jan 2024 22:57:23 GMT  
		Size: 13.4 KB (13427 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:8ef5e41feb50237e8c43397d0e9d6eb3b5e10da48305f59775b017d958533c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117296421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d942e0e41dd9033eb65f8cae831cd102ab1031a22bb7b0687aae4d9dfd6a2b7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.7
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
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
	-	`sha256:87a587152db2b1ea855e67d76552789d0a223539d8a5f3c26ebf47ff6110d421`  
		Last Modified: Wed, 24 Jan 2024 21:24:02 GMT  
		Size: 17.2 MB (17167108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb9103a5bcf6341ed5a6642ccc156df851096386361a118d94fae7a95c63f8`  
		Last Modified: Wed, 24 Jan 2024 21:24:01 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea6f9c68b132ef951940ee038d8c4eebb31eaf693a359164a694ab3a9de1c79`  
		Last Modified: Wed, 24 Jan 2024 21:24:01 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3ff5e0540022abd755f8273a5fff3a3a24c7bf2f0215d7490263e8b6a221a`  
		Last Modified: Wed, 24 Jan 2024 21:24:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acb34603f7509bef4b6ca9c0feafa0e0d893333ba2cafa5dd980715c39c8c3f`  
		Last Modified: Wed, 24 Jan 2024 23:23:50 GMT  
		Size: 8.4 MB (8396023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d52caa0bd52734766b496186d72e86a9118919055f143c3fec478ed68b7189`  
		Last Modified: Wed, 24 Jan 2024 23:23:49 GMT  
		Size: 78.9 KB (78884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850a1a5bbc8fa29faf2c504d619d830a24531dab08d86d9f61cbea47e3896c18`  
		Last Modified: Wed, 24 Jan 2024 23:23:49 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd90affbd5a7d6d56328789a1b0999816972d5635c9570245c958747721e087`  
		Last Modified: Wed, 24 Jan 2024 23:23:51 GMT  
		Size: 51.0 MB (50964341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a743afa6c9eee0fc3b76b10f6e9fbd66d8d7e5fd7889cfb513edae2a679f8033`  
		Last Modified: Wed, 24 Jan 2024 23:23:50 GMT  
		Size: 1.5 KB (1507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834b58a12330c8dc1c724c447777560047cfdb9a636a9db1f2eb4615ccc62c8b`  
		Last Modified: Wed, 24 Jan 2024 23:23:50 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbef5abec898628017d5614b4650ae7a15309cb31e34f0df0cf56bc156a20ad7`  
		Last Modified: Thu, 25 Jan 2024 00:11:05 GMT  
		Size: 4.7 MB (4663248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:e3eda41b92c6b74a9813caa9dc58321807862d576ad45d8bf603a42fc7b9f421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **762.6 KB (762648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a582e053114b719177ac55303d7297d4e2ba2478d3515e7fed2fa51377ac3e10`

```dockerfile
```

-	Layers:
	-	`sha256:c6a043d4546cccf481cb5684fa682b8e2a2678a5ff962b8c6f90961602d8ea8a`  
		Last Modified: Thu, 25 Jan 2024 00:11:05 GMT  
		Size: 749.0 KB (749005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:232254567c4c6c1cfa11707dca4fd42bf1668ac09d7db85a7363f7c219d90648`  
		Last Modified: Thu, 25 Jan 2024 00:11:04 GMT  
		Size: 13.6 KB (13643 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7fbb4df342d5f567217310ec4e3c6f02379e345011e9a9490b720b428a3ad279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117618826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fd8a9c3b825e7339f6eefee57ef3216e0626c0b0d72b2f3765488a96370f89`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.7
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.2
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-x86_64'; 			sha256='067a12983b9333d01947329190af756b6d12afe7b4b51b3e1e29328b4afe3b9f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv6'; 			sha256='582d734ef0c14335ee4691f3550d56b3e1c1c4d787ed6354830b3c222eee542e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv7'; 			sha256='e83fa84dc73cc8d5a0fe2d1ad3ad61202050f033e6df9f3f4f7b3c2b59181006'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-aarch64'; 			sha256='beafe762fedd06fe9885317c33f8b29b39c2354d6840a494a69b3c3a36919212'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-ppc64le'; 			sha256='6be73d6597efc822eff3f9dd6abb56b72ada76f8a5f798b1df2dce5105f39257'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-riscv64'; 			sha256='33a15fcef9d975aee4ed404779fae068264da6de8f2851ead85f9e1701302411'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-s390x'; 			sha256='0b62a8d7aad7ce81220a4d77aa4b17e443b888248c1da22bc808db1fcbf1e9ac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
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
	-	`sha256:66a65a5d845c7fe812cc8a9e6d4ce6d607db0d56f63829bf7696c3677559c178`  
		Last Modified: Tue, 23 Jan 2024 01:47:29 GMT  
		Size: 16.6 MB (16607524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b105404b288db3b76414d96889520ba1d80a776d6e83816700fd027da04df95`  
		Last Modified: Tue, 23 Jan 2024 01:47:28 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a0ea407ba895072c0de38ee6ae87403a9a6fa480300b1d4a144e04d8e4313e`  
		Last Modified: Tue, 23 Jan 2024 01:47:28 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86978bef749e39bfd2b2535fdbf958097586a891064f3aca97c33bbd6147908`  
		Last Modified: Tue, 23 Jan 2024 01:47:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817a0104370e84f1bd2e04835f107b7e34bedc407463f8c419a0a91b1aa2182d`  
		Last Modified: Tue, 23 Jan 2024 03:40:57 GMT  
		Size: 9.5 MB (9509875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a630eb276944682f6c6d9e493fcbbb3f4a5488eb2cca382d1a1ed468314203`  
		Last Modified: Tue, 23 Jan 2024 03:40:57 GMT  
		Size: 93.1 KB (93083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b6d7049541bab4337b78f34e4326239182a6e5b1461134e2e00391d2ebf1d4`  
		Last Modified: Tue, 23 Jan 2024 03:40:56 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995bd3ad158a4e5b00d51f66333eeccfb3db1b6594b0fec5e6683e66300a565`  
		Last Modified: Tue, 23 Jan 2024 03:40:58 GMT  
		Size: 49.7 MB (49711211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168e5732b24dd62b475b52ef3cc2ac0690998e1b68fcb9e136a755b9dc5af27b`  
		Last Modified: Tue, 23 Jan 2024 03:40:57 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41f66197e21910a96e02a4e92704bee177b4d55322e576e010408dc9a8ce0ad`  
		Last Modified: Tue, 23 Jan 2024 03:40:58 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca21573dead4d08b7835f939ec7b30b055625ef6da8f24fdf4c3fd9057920e5`  
		Last Modified: Tue, 23 Jan 2024 04:31:56 GMT  
		Size: 5.2 MB (5235972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:97b2dd21e8da6130b7492c0dd9da2122308687957375e41e8090fc755c60bf9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.6 KB (757595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e708bdc8becb0f293e709bcb7ad7efef73494cc9be8fb3763fd41c2d801b8b`

```dockerfile
```

-	Layers:
	-	`sha256:ae1cd2cb65f1e1da778d3195ca9f4d7b068a99654e0e8f159581c2fbeb2115d7`  
		Last Modified: Tue, 23 Jan 2024 04:31:55 GMT  
		Size: 746.5 KB (746515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4007652c9fa4fdb9e21b487354660bfde9387642d48cd39585b7738a8f0eb0e3`  
		Last Modified: Tue, 23 Jan 2024 04:31:55 GMT  
		Size: 11.1 KB (11080 bytes)  
		MIME: application/vnd.in-toto+json

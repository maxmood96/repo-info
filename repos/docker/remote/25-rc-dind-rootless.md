## `docker:25-rc-dind-rootless`

```console
$ docker pull docker@sha256:de59338a02652249c9f667ebebf98e9e7e126b986dc0c2642471ba2e6ba94cc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:25-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:669306b7927d2c788a4c5d50cc3211c796c2506fbf83025fcca0c40066911d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144530078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9972609116c8bf5f31ecee07bea789cfa3d530fc83bdf9cb2fc9b413cfed7d4e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_VERSION=25.0.0-rc.2
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-x86_64'; 			sha256='43fb39c0bc24ac796123935032eddcfb57a7acd9216badeb10714c986ea1e090'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv6'; 			sha256='cb407cfd396892cc0317ef48570492d7e59445a9f50e92181fdf637548801d55'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv7'; 			sha256='936b474e24a51a51fd797bd18290da6abf72d62a614d8730a1fed3deae816ed5'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-aarch64'; 			sha256='d23d03be5880a2f6555932c572ddbc87bd0e1c4c1985933b7488d948eb2494ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-ppc64le'; 			sha256='f52678e23b143b26c2ee20af4ac105ed571bb2e8e39d59478e04bd2d81cbe27c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-riscv64'; 			sha256='555a373414675ae21cafff8280346c94561457f4be254b5576b22f4b5e8f2ab2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-s390x'; 			sha256='37871d879aa0a73f2ac59dab9805bee751d25208bbe72d7d2ab45956f2e1750a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 13 Jan 2024 00:58:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
CMD ["sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
VOLUME [/var/lib/docker]
# Sat, 13 Jan 2024 00:58:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 13 Jan 2024 00:58:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
CMD []
# Sat, 13 Jan 2024 00:58:33 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-25.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-25.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 13 Jan 2024 00:58:33 GMT
USER rootless
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b7f064c01b1bb00930b3e01703d33a3722bc48570f05caabe254fa622d5b11`  
		Last Modified: Sat, 13 Jan 2024 01:55:53 GMT  
		Size: 2.0 MB (2018470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6384ba132479eeed7dc2a53d25983e63aa3f6154460441fdb1a3e3f7a80443e7`  
		Last Modified: Sat, 13 Jan 2024 01:55:52 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925fa9b01434370f38b386a384af6d0cfac8d48915687812313cb0ac0a56d2bc`  
		Last Modified: Sat, 13 Jan 2024 01:55:53 GMT  
		Size: 16.9 MB (16893464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b7ecf52b17acaf42aea5c9db0fc3cf2c7200d2decc8772147016efa6ae5b5e`  
		Last Modified: Sat, 13 Jan 2024 01:55:53 GMT  
		Size: 17.2 MB (17195298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e2b37a68e23c28aeb3a824f509fd6aa0af4e44a8c13ea0dc404eaaccc8f265`  
		Last Modified: Sat, 13 Jan 2024 01:55:54 GMT  
		Size: 18.2 MB (18172990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29174eeb0beb2d30a18ef5f97f20708774acd7dda13ecd162ac8031642859f54`  
		Last Modified: Sat, 13 Jan 2024 01:55:53 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f70c9f92f25c65b317150b377ebe33464f21796e7d63465db037d357623426`  
		Last Modified: Sat, 13 Jan 2024 01:55:54 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34dbdd19712963316234ef84221fcbddf7c9adc6ec9940333d65beb0ac06407`  
		Last Modified: Sat, 13 Jan 2024 01:55:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09307a47c237fef0b49729e2e08b57fb7bb2653fb299b68804048a2f4ac62e62`  
		Last Modified: Sat, 13 Jan 2024 02:48:23 GMT  
		Size: 9.3 MB (9258187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5db6e646404533bf4455f687188ba9552895a3fa1eebe58f6c6f7d98e8045b2`  
		Last Modified: Sat, 13 Jan 2024 02:48:23 GMT  
		Size: 83.7 KB (83650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc912980e90ff83ee0471cfa018c98fa490fd5e47c4027f9853bd392353621f1`  
		Last Modified: Sat, 13 Jan 2024 02:48:23 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180886f8420a98e990b897f34b1ffb9149022a2fd149745f5872a35a8dab1ec1`  
		Last Modified: Sat, 13 Jan 2024 02:48:25 GMT  
		Size: 55.6 MB (55627779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d0a9fe2149e51b444c1b27318f1c48d18f15713b9e08a78e2b368a447de970`  
		Last Modified: Sat, 13 Jan 2024 02:48:24 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e478b3ea416cf1f0dd7a23539c773d2886b55868f07d7cb0a29aacb7fad343`  
		Last Modified: Sat, 13 Jan 2024 02:48:24 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5433b4f041b85937a7e99345fff49b8735bd546eca8e4e93744a704d8263a121`  
		Last Modified: Sat, 13 Jan 2024 03:47:49 GMT  
		Size: 974.0 KB (974048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e30650903d90f54b17d9843120df4893cf30060c2a1522761715bce500ab2e7`  
		Last Modified: Sat, 13 Jan 2024 03:47:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7387415aee5bdb3d985d150bb05fa1e6bee72c8cd4a0ee84084260d2fee73b`  
		Last Modified: Sat, 13 Jan 2024 03:47:48 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17c0139ff23a76359dbc77d094c13379674e55ba9dfb644124486daad43540a`  
		Last Modified: Sat, 13 Jan 2024 03:47:51 GMT  
		Size: 20.9 MB (20887757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d677253f8c0275678cbd1498f404612a4c7abf1e5fe29b1746c28607db1c37f1`  
		Last Modified: Sat, 13 Jan 2024 03:47:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5e85a85cc882c279c8f5c528226f0193ded2f38a4063f011b9a564522da1053a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10b0f4072eb099fd3938f2419cce3a204785c187004c91c254d913be0fef0d3`

```dockerfile
```

-	Layers:
	-	`sha256:b6309a0a336f2ea7524f5255e4520725aac599e86602dad8b0388d38c41e3f20`  
		Last Modified: Sat, 13 Jan 2024 03:47:48 GMT  
		Size: 736.8 KB (736833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243814a422f41ed02acf285c46cb5518d8d29b12eb19af33dea753262518b111`  
		Last Modified: Sat, 13 Jan 2024 03:47:48 GMT  
		Size: 33.0 KB (33001 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:895d291ed6fb17fe08f380b8d8f08bf87221e7af297cd104fa968e7412b54606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138226847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626750a63e69f0e8ced1f77e3ba1f1a552ca57dfb16c256525292a8af19464af`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_VERSION=25.0.0-rc.2
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-x86_64'; 			sha256='43fb39c0bc24ac796123935032eddcfb57a7acd9216badeb10714c986ea1e090'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv6'; 			sha256='cb407cfd396892cc0317ef48570492d7e59445a9f50e92181fdf637548801d55'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-armv7'; 			sha256='936b474e24a51a51fd797bd18290da6abf72d62a614d8730a1fed3deae816ed5'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-aarch64'; 			sha256='d23d03be5880a2f6555932c572ddbc87bd0e1c4c1985933b7488d948eb2494ca'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-ppc64le'; 			sha256='f52678e23b143b26c2ee20af4ac105ed571bb2e8e39d59478e04bd2d81cbe27c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-riscv64'; 			sha256='555a373414675ae21cafff8280346c94561457f4be254b5576b22f4b5e8f2ab2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-linux-s390x'; 			sha256='37871d879aa0a73f2ac59dab9805bee751d25208bbe72d7d2ab45956f2e1750a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 13 Jan 2024 00:58:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
CMD ["sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
VOLUME [/var/lib/docker]
# Sat, 13 Jan 2024 00:58:33 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 13 Jan 2024 00:58:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 13 Jan 2024 00:58:33 GMT
CMD []
# Sat, 13 Jan 2024 00:58:33 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-25.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-25.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 13 Jan 2024 00:58:33 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 13 Jan 2024 00:58:33 GMT
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
	-	`sha256:ac9ce9355c7eac1b612e968f40710754b6f67908ba443da9fdf04e8ffeeb9418`  
		Last Modified: Sat, 13 Jan 2024 02:32:52 GMT  
		Size: 15.9 MB (15901428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8868d84a8d0f0227f035dfc69bf4d0b7fb5dd196163d55d834724bfe8c4eca3d`  
		Last Modified: Sat, 13 Jan 2024 02:32:52 GMT  
		Size: 15.6 MB (15640597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced2fea1225571c5444ed013200c3e5a448e255f93d62d524568e8eae99c5e67`  
		Last Modified: Sat, 13 Jan 2024 02:32:52 GMT  
		Size: 16.6 MB (16608012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72ce2a51daea36c908727a2d1d6d0b5010b0c5930ac86b2dd114769b8433d9c`  
		Last Modified: Sat, 13 Jan 2024 02:32:52 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5a1ab4f0bfc9487191e3c211da3ef8fbe55cccbe8c45218b48c74ad689827e`  
		Last Modified: Sat, 13 Jan 2024 02:32:53 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c04de793f9276bc0c4cc72a94991881f4c9159a54a67f62a240eb69440802f7`  
		Last Modified: Sat, 13 Jan 2024 02:32:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a4e456a3769ad1fd04e0361fb0a656f5d1f732fcf61d2eb6b520741f8d11ee`  
		Last Modified: Sat, 13 Jan 2024 03:13:58 GMT  
		Size: 9.5 MB (9509861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371b97e04e2bc3dd9bc40848bf73181c40a9c407649b09a0bcfaef20dca6c141`  
		Last Modified: Sat, 13 Jan 2024 03:13:57 GMT  
		Size: 93.1 KB (93074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934f3100eb3bc611042431efec97bbb6931c8e002875945aa5e08d452a967536`  
		Last Modified: Sat, 13 Jan 2024 03:13:57 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67febe004548180d4f9cbe0e21d083984a2e69d1aed78260f1d5763b60ef3a1`  
		Last Modified: Sat, 13 Jan 2024 03:13:59 GMT  
		Size: 51.3 MB (51339507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84452ae9f87c07fe681152d22c825b39a7f2f40eefad39489fa43eb6989573ab`  
		Last Modified: Sat, 13 Jan 2024 03:13:58 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a66f44ad12dee29dcebfa71b4f553860751ba7bf5ca3078262d85d67ff6670`  
		Last Modified: Sat, 13 Jan 2024 03:13:59 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0c30fe1eca051a88193c283a83765d6337748c3711d59b7218258a38308525`  
		Last Modified: Sat, 13 Jan 2024 04:18:56 GMT  
		Size: 1.0 MB (1016234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded93363f2fa162c42b7add60ce804a1349f499bf895e11fe8b1a6339cb7c170`  
		Last Modified: Sat, 13 Jan 2024 04:18:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eef9c0815b568df6a3d4ea3f174daaf5a080f1edd654d2cf20e8d3827cdf16`  
		Last Modified: Sat, 13 Jan 2024 04:18:55 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09261073276d16f9aefd03bf6a2c19937c1906d4ccff66fbb6f9065630f84c73`  
		Last Modified: Sat, 13 Jan 2024 04:18:57 GMT  
		Size: 22.7 MB (22745489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495a97b8439e04d325f81c0001b867906cf68956179560ff26598632ee08c501`  
		Last Modified: Sat, 13 Jan 2024 04:18:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:66ac413138e620185908c6554c7d9a5181c11aacef92c2a3e634723dc6b5b77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.9 KB (769904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ed606a55c6a09cae23c1b2336e6627669dedc06fee466f2b586bae29aaa2f8`

```dockerfile
```

-	Layers:
	-	`sha256:39dbc371f87b56e32db5510124bd38055b1e6c6006d03b5df1677835a0de28a6`  
		Last Modified: Sat, 13 Jan 2024 04:18:55 GMT  
		Size: 736.8 KB (736842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0471765a64684e540e7b2a07e7994b39f44728cb1a27783ee9a9cc4f5342cc7e`  
		Last Modified: Sat, 13 Jan 2024 04:18:55 GMT  
		Size: 33.1 KB (33062 bytes)  
		MIME: application/vnd.in-toto+json

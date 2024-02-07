## `docker:latest`

```console
$ docker pull docker@sha256:9abbaf8bbbef41f496396f897220934b375aad8b54ac6c6707687c59e1c598e7
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

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:294bfcbbc5589fdc4f7e32864b08eee7d41a45856af541e1b000f8038ebf3c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120524093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7da5c2b684680135f3c21ff5550f166c3100f3a664292c24b8d4491591157c`
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

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:2f0e477a2abecaffa0504051e1776ed4da08a56ab5402f9d5a421829ad7dfac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.4 KB (730427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3e59983d30014064f422144f99cbedf558ded8abdf7bd76f2e227c61d7cec0`

```dockerfile
```

-	Layers:
	-	`sha256:1658b15b5744890353b17c7d6f8bbb4fe9804dbbf1584ec74e4fa5225eddf299`  
		Last Modified: Thu, 01 Feb 2024 19:56:54 GMT  
		Size: 693.4 KB (693444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe34b47ba4e634d7b52af58a9f83316b129f5779cb5b61fd8f7252b809cae51f`  
		Last Modified: Thu, 01 Feb 2024 19:56:54 GMT  
		Size: 37.0 KB (36983 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:6dcd9349f1f0c5398ad3dddf9679babdcd5ff4d03183c10a662b8d551b1d6381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113323731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68f641892526a3ba5dc180e4e1ca8a19b972886b02c6f856bd298d5e1aff94b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
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
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535f449eaa17419820b7f0663934df7e5beec16d62e48ea67af70de00c66ad05`  
		Last Modified: Thu, 01 Feb 2024 19:04:43 GMT  
		Size: 2.1 MB (2108649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4e66b84d1f5f9f16d502669f3a99b2cb66c56f82a552d43572bd2e2a036329`  
		Last Modified: Thu, 01 Feb 2024 19:04:42 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8d0f81de62948e97140c7bb54c7b8ae87d4e44c3fa63116027c6458993e3bd`  
		Last Modified: Thu, 01 Feb 2024 19:04:43 GMT  
		Size: 15.3 MB (15271625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661f1ffa4117f582b42a8aa9f5250cf1b0c6349b4f0a08368fc8f5fc73ee4f5`  
		Last Modified: Thu, 01 Feb 2024 19:04:44 GMT  
		Size: 16.1 MB (16099977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37410c7002d24163b2a278f4455e6c0364e2252449f14bead9d9478b289154f0`  
		Last Modified: Thu, 01 Feb 2024 19:04:44 GMT  
		Size: 17.2 MB (17196912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca4dade56f5db9cd770cd5c5527771ac24d17c2f3953853d83e79ea8cd4a0`  
		Last Modified: Thu, 01 Feb 2024 19:04:44 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee486b19bfe5900ba205e3e835be605877777823a22aa747a011f5cab96f4f5a`  
		Last Modified: Thu, 01 Feb 2024 19:04:45 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594b71c85446ef661d393b3751883b4dcd763ce67fbc3f77eba3d45262c61c41`  
		Last Modified: Thu, 01 Feb 2024 19:04:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33505063f1758463655bba0d441f495471a872d42247d61404080069cc7b736`  
		Last Modified: Thu, 01 Feb 2024 20:04:48 GMT  
		Size: 7.4 MB (7362155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb20dad9e684795fc70899353d986ff01d150c8ef70b11339162a8acdd9dff9`  
		Last Modified: Thu, 01 Feb 2024 20:04:47 GMT  
		Size: 82.6 KB (82598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba1548be80e27c0226d017712792a3b36ed3e1170df53ab53420200d49610a5`  
		Last Modified: Thu, 01 Feb 2024 20:04:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da77e8203deabbe5ea7f6571809ea015ac324cd54942d1113ba8f401a7fc8841`  
		Last Modified: Thu, 01 Feb 2024 20:04:49 GMT  
		Size: 52.0 MB (52028099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6608d3dca1170a1d3045b6695007085f139dd2bfda8f58c3f0546c4effb3e05f`  
		Last Modified: Thu, 01 Feb 2024 20:04:48 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ec9d56a5aef31130823d8a42a163d785c36f94ea1faeca7cbfc9345c7e6484`  
		Last Modified: Thu, 01 Feb 2024 20:04:49 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:305e74a75d3a8ce61c3e7588b648cdc44cc2367b3fdd402b810d36a9323f1d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (36992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1dfbae0ba98af8ce7c3aab505fce3983ca6c2fcf8e6c8896fa042ad14ed2ec`

```dockerfile
```

-	Layers:
	-	`sha256:8d1382eb99c40afe8489474154ce21772e701ecd9ddf1336346b97b15a4449b7`  
		Last Modified: Thu, 01 Feb 2024 20:04:46 GMT  
		Size: 37.0 KB (36992 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:97354094d74920f349c7687639528353c732159aeb91f76fcf083ccfaf031489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112111872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac654c8250a96d88233b48dfc0061e37148508609680a8f67f02a920a0458729`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
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
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d7567cea9b984ed5ef416f6b88dae89cc6ee911a3c07a56bec9cb5e3db80e0`  
		Last Modified: Fri, 02 Feb 2024 14:52:46 GMT  
		Size: 1.9 MB (1896180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5f991740564aa851e62aa9c5fcc779094c0abfbee45897b4eefb30712b6112`  
		Last Modified: Fri, 02 Feb 2024 14:52:46 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387dd610fdf7ae43e9c940a411be2bd24d884da3a1732f0ed6227460edf13ce6`  
		Last Modified: Wed, 07 Feb 2024 02:15:08 GMT  
		Size: 15.3 MB (15269408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b557423f8bc23bf5bbf745e871e82c8e621a448ab751b5ff3b1046324f86c4`  
		Last Modified: Wed, 07 Feb 2024 02:15:07 GMT  
		Size: 16.1 MB (16084092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9615b4c0f37088aed8ee74a32dc58bbaf47828ac09a3db3d7b314618f54241a7`  
		Last Modified: Wed, 07 Feb 2024 02:15:07 GMT  
		Size: 17.2 MB (17175377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3203bebd5f0cbcdaaeb72e79edfca9ab9c584d1bf755c8e794b77f5d553951`  
		Last Modified: Wed, 07 Feb 2024 02:15:06 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91201bc30d6259ead7a888a45d05f66e759813442b3a09226b6a1874dd3b5691`  
		Last Modified: Wed, 07 Feb 2024 02:15:08 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf89b89eab09953c662097632f751c1cc408623f7e2ce409f9047c8321803349`  
		Last Modified: Wed, 07 Feb 2024 02:15:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8f99bf2047898829747bd3314b7daeab13ccd23255d2dec45774d43f672880`  
		Last Modified: Wed, 07 Feb 2024 03:40:32 GMT  
		Size: 6.6 MB (6649816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba5541bd9ea17ba83aa26131ecae1b17a29b7a222d5a1533c13f6b7d16ab4b0`  
		Last Modified: Wed, 07 Feb 2024 03:40:32 GMT  
		Size: 78.9 KB (78887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de759b1eeb0a433e7188058c4c98b2643d03250cdf4e8424cac3807759d360e`  
		Last Modified: Wed, 07 Feb 2024 03:40:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4638a4a9cc3d4cc59049ae90ececc81c0362ad2788e777c94eaf3af90b6c88a8`  
		Last Modified: Wed, 07 Feb 2024 03:40:37 GMT  
		Size: 52.0 MB (52030894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812f45e94a82ac0f0665f2ebfab47628f18733fdf561b95c3c42edea615bcf56`  
		Last Modified: Wed, 07 Feb 2024 03:40:33 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bfcf945f8fabb9410ed13c63688eda287e5c8e1694c7dbd5bf3d2b7e8f2f08`  
		Last Modified: Wed, 07 Feb 2024 03:40:33 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:b836f12139e632159518a402a934a752ec1b9e2e7da1508c3483033a3a840671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.0 KB (737986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0228a4ff00704b25ad2332421ddbbb7442b480219caafef993ed99763f4ae8a2`

```dockerfile
```

-	Layers:
	-	`sha256:1b776d266bbb436a2c39f395bf29fba8118fa3c99ba3ae0815f39a995fdcd381`  
		Last Modified: Wed, 07 Feb 2024 03:40:31 GMT  
		Size: 700.8 KB (700779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c42391fe856bfbc71da29db7795ce412beb5dd7e3fce63ea45fc74e387941b`  
		Last Modified: Wed, 07 Feb 2024 03:40:31 GMT  
		Size: 37.2 KB (37207 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a0033ee30d87d9255fcec7bda4171da530dc134fd1d68a4ec7a1af1a9b54adc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112414564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420ae8c00cdf6f95c4d4115209ad440aaaf750a871c97c1f5a67b5f04628f8bd`
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

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:7c4319183a3e7fe811e619fd4752531245e4b1710149a96f47c2e84d8e58f9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **737.8 KB (737777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3f9a09009f79870b7ee8665e1cfebd0c3283c47cfb96b8031a0ff4db0e65d5`

```dockerfile
```

-	Layers:
	-	`sha256:279755656c3c79714412a73bd52b47d5f69f5376c33327cdaf59fd51f3d67dde`  
		Last Modified: Wed, 07 Feb 2024 03:27:07 GMT  
		Size: 700.7 KB (700718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0ca2fa7f87c8011730434f332b17be533a5502f7357059ff07b0faeb29dd6f`  
		Last Modified: Wed, 07 Feb 2024 03:27:07 GMT  
		Size: 37.1 KB (37059 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:25-git`

```console
$ docker pull docker@sha256:fee7669f2beebc684a1548bd58554790fc114a2b71b5ba51b005e4b94c2e8e41
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

### `docker:25-git` - linux; amd64

```console
$ docker pull docker@sha256:0b73c87f72cc1c7d56b9686a4a08dc8265e9fb023c4c9ffa0bbf68568e6aad8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125654276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2c3b17a69965b4125d9f848037ddf3e55b63b9a7580288de173e78454b7a29`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 19 Jan 2024 12:04:26 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Fri, 19 Jan 2024 12:04:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_VERSION=25.0.2
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.5
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-x86_64'; 			sha256='94355be1d1d395040bbda1490f98d5c7627c30798a7955e1f2a78fda33a4b3e1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-armv6'; 			sha256='bd402cf44fec9640c29e85184ddd36c9d4094045b296e2833533d53715d0cfc2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-armv7'; 			sha256='80248b4c2c407b22b24896ff6d6e766be7ca97239c5b8137f47c81b62a1befb4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-aarch64'; 			sha256='535e90ff9a7f24384f8a38f9f9ad49125485af7ae5ffda7226d091e5b8126948'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-ppc64le'; 			sha256='2143fd5df30c29e22869e5461afac0ca1f2b8d435c544b89fc1d826eb9e52df8'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-riscv64'; 			sha256='e4534c48b1bdf68d664ccc426800b215d3708f3a492d57e36b0a412f4d229546'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-s390x'; 			sha256='7def69d38989d1020c49ab37bb68ab2c29558484e33fc952b5258c84cb1bbda1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
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
RUN apk add --no-cache git # buildkit
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
	-	`sha256:0562ef117a7efdf99cc159585630d529a75cd47a863ef7cccc3b4c07e2fa4b7d`  
		Last Modified: Thu, 01 Feb 2024 20:56:35 GMT  
		Size: 5.1 MB (5130183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-git` - unknown; unknown

```console
$ docker pull docker@sha256:4f8b428d590b1465bebc4ca69b05c88c37ee5cda4c54f44700ba25c3d4a7dfec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.5 KB (752549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206e6631baf1c820d4962aa35488b6725b8ae9b895f96e26a5439f696dd65ad2`

```dockerfile
```

-	Layers:
	-	`sha256:6acab0f4775f389dcf81480f05a2d43e0559c2838fb7b0f13de5a699c64969bf`  
		Last Modified: Thu, 01 Feb 2024 20:56:35 GMT  
		Size: 738.7 KB (738700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:878230669fb5ed379d67df5886a0e668032abefcc55c38cd70dfac180b36e0be`  
		Last Modified: Thu, 01 Feb 2024 20:56:34 GMT  
		Size: 13.8 KB (13849 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:52cadc33ea76ab73977f8a5d86891547eb29eca1c2243d0486198fa9f0d55966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118429675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271673c938fc0efe6b54399e9758fe40bc72cbdea6682eb20dfbc27a47da0fc9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 19 Jan 2024 12:04:26 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 19 Jan 2024 12:04:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_VERSION=25.0.2
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.5
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-x86_64'; 			sha256='94355be1d1d395040bbda1490f98d5c7627c30798a7955e1f2a78fda33a4b3e1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-armv6'; 			sha256='bd402cf44fec9640c29e85184ddd36c9d4094045b296e2833533d53715d0cfc2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-armv7'; 			sha256='80248b4c2c407b22b24896ff6d6e766be7ca97239c5b8137f47c81b62a1befb4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-aarch64'; 			sha256='535e90ff9a7f24384f8a38f9f9ad49125485af7ae5ffda7226d091e5b8126948'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-ppc64le'; 			sha256='2143fd5df30c29e22869e5461afac0ca1f2b8d435c544b89fc1d826eb9e52df8'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-riscv64'; 			sha256='e4534c48b1bdf68d664ccc426800b215d3708f3a492d57e36b0a412f4d229546'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-s390x'; 			sha256='7def69d38989d1020c49ab37bb68ab2c29558484e33fc952b5258c84cb1bbda1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
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
RUN apk add --no-cache git # buildkit
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
	-	`sha256:97165ed5b6486c69d51ab434a4e3121e675e8e0067ef27346daf93e3bf10cf2f`  
		Last Modified: Thu, 01 Feb 2024 21:04:31 GMT  
		Size: 5.1 MB (5105944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-git` - unknown; unknown

```console
$ docker pull docker@sha256:d26fc3e0a426e2cf7c1746ea78d02cf6aff0634b1598e5af85bff592b20cf00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823d398a5654fb7a7f146953172900513561bb94b5d8484b78e3bfa230171b71`

```dockerfile
```

-	Layers:
	-	`sha256:104df3cdeac3b87d65fd4cef0dace6f8bafa334a483f7ff65817351d8d111cfc`  
		Last Modified: Thu, 01 Feb 2024 21:04:29 GMT  
		Size: 13.7 KB (13728 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:7211a68f20be1c238539c04d6468c268a8c6c3e4e4df1efee2b385a95df872c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118488108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0ae848486f7abd800da33f29ddf2ba0350b8ff512c1140bdbd1f280be21515`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_VERSION=25.0.1
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
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
	-	`sha256:0f55303c45fe6e4ceb7ded22a5f4ec82d6e3b944ff5fd0e34e946c243b5516fe`  
		Last Modified: Wed, 24 Jan 2024 21:23:33 GMT  
		Size: 15.3 MB (15267848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad337070384e9cdad75d659ecbb01b57477deec88cdb8930ab1957401a603510`  
		Last Modified: Wed, 24 Jan 2024 21:23:33 GMT  
		Size: 16.1 MB (16084092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17194f54b764ad754e9cc7416d766f62d8453e0eb079aa81d2ce25b3fecee940`  
		Last Modified: Wed, 24 Jan 2024 21:23:34 GMT  
		Size: 17.2 MB (17167101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74638158749a678b151340fe7395474f1359c91bfaa3dbb267feb61f1aadd6c5`  
		Last Modified: Wed, 24 Jan 2024 21:23:32 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a740ec1e118a9ce8469d40e651a926ed6527c2e831484696aaf10b598cfd262`  
		Last Modified: Wed, 24 Jan 2024 21:23:33 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa26e96e66e48f6a9b5ed79a0e180d47d01af19a94bf6d5796b93275d4895d30`  
		Last Modified: Wed, 24 Jan 2024 21:23:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5231f97639f35eb16d696e9bae2943b5a683a9b8da396e4721b7fc91a0b64cf`  
		Last Modified: Wed, 24 Jan 2024 23:23:05 GMT  
		Size: 8.4 MB (8396023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1241b26d52651249c2c812cf0e941033109efad56cfeed5563a0698035e8e7a`  
		Last Modified: Wed, 24 Jan 2024 23:23:05 GMT  
		Size: 78.9 KB (78890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effdea191a7f03c686f397ac4776acbc3c955d5092583e818008ffeb6892c022`  
		Last Modified: Wed, 24 Jan 2024 23:23:05 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05081d7c121bc68e75b5af60073c9ea64daa8fe5e7302174e9ea1e348b1f93e9`  
		Last Modified: Wed, 24 Jan 2024 23:23:07 GMT  
		Size: 52.0 MB (52015254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00040411c0b6749fba8619084ded52ecf9f46e8425ee39159b7e45b38a348a`  
		Last Modified: Wed, 24 Jan 2024 23:23:06 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3da45a47a2bdbe62195db50347c0e34cfef571638fe50744f7cb172b97ed29`  
		Last Modified: Wed, 24 Jan 2024 23:23:06 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81871100d1fb7fef9fa1ff49a729d15fd5e990e8fa1482758a6cfcc07bf5b4be`  
		Last Modified: Thu, 25 Jan 2024 00:10:39 GMT  
		Size: 4.7 MB (4663229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-git` - unknown; unknown

```console
$ docker pull docker@sha256:f3a7c7cb0c0262d30f6b4e473542bb5f6728935ad0e810247a61a0aae88ebf53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **755.6 KB (755645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88e2db92025f3fcab8c34d5e9a31e5806359f75a72283dd6e84f6342cb2a061`

```dockerfile
```

-	Layers:
	-	`sha256:6299eeb57033ae9f72168275e0fb657629ac26e0777b32e78254225cebf1324c`  
		Last Modified: Thu, 25 Jan 2024 00:10:38 GMT  
		Size: 741.7 KB (741702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a7530ea11a22f4327671598c68644ff669e13a15bbcda03302953d84b564815`  
		Last Modified: Thu, 25 Jan 2024 00:10:37 GMT  
		Size: 13.9 KB (13943 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:51adfa26452cacebd37914ac9812f70613045180e4f7a6da8e7adf06d958b8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117648997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5370088faf49262d02ba2f2f2175e34d4d1387a3c1597e886666e488aa39e48`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 19 Jan 2024 12:04:26 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 19 Jan 2024 12:04:26 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_VERSION=25.0.2
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.5
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-x86_64'; 			sha256='94355be1d1d395040bbda1490f98d5c7627c30798a7955e1f2a78fda33a4b3e1'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-armv6'; 			sha256='bd402cf44fec9640c29e85184ddd36c9d4094045b296e2833533d53715d0cfc2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-armv7'; 			sha256='80248b4c2c407b22b24896ff6d6e766be7ca97239c5b8137f47c81b62a1befb4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-aarch64'; 			sha256='535e90ff9a7f24384f8a38f9f9ad49125485af7ae5ffda7226d091e5b8126948'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-ppc64le'; 			sha256='2143fd5df30c29e22869e5461afac0ca1f2b8d435c544b89fc1d826eb9e52df8'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-riscv64'; 			sha256='e4534c48b1bdf68d664ccc426800b215d3708f3a492d57e36b0a412f4d229546'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-linux-s390x'; 			sha256='7def69d38989d1020c49ab37bb68ab2c29558484e33fc952b5258c84cb1bbda1'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
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
RUN apk add --no-cache git # buildkit
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
	-	`sha256:63b9aa678396ae75491b9b74ec59dd9c740e92ad698d62a2c7a5d14fce5105fc`  
		Last Modified: Thu, 01 Feb 2024 21:53:48 GMT  
		Size: 15.9 MB (15901605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fb2c4ff3d6decc271266cbcd082798d2c7f55d91fe2ad0a5c3e3006272b99c`  
		Last Modified: Thu, 01 Feb 2024 21:53:48 GMT  
		Size: 15.6 MB (15640600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02ac4bd2008cc5cf6b2a3fb7cfa9736d7ecfe12fabf1a15553796ffecfaf6d`  
		Last Modified: Thu, 01 Feb 2024 21:53:48 GMT  
		Size: 16.6 MB (16619361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2009dfc85eee07395c90935b7d3b4e3b4b15fd2cf005c92de8be85853a4ade1`  
		Last Modified: Thu, 01 Feb 2024 21:53:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2658d0b3337bc55789836b68f551de35ac0cb99f6c432b1629fa07761110d3ee`  
		Last Modified: Thu, 01 Feb 2024 21:53:48 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3b9ec2c9140d9e3ddb2d362c1156bd408e6d0e844bee172dfbe0b50e50f724`  
		Last Modified: Thu, 01 Feb 2024 21:53:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c6471df5d5da8e0c360a0e6eb99c38cb88735d6cd0cdfb104e6036628f82a3`  
		Last Modified: Fri, 02 Feb 2024 21:56:07 GMT  
		Size: 7.4 MB (7428496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c5b2211658fb2142feb2f395199cdce355279256bde43981e7e0aeda710211`  
		Last Modified: Fri, 02 Feb 2024 21:56:06 GMT  
		Size: 93.1 KB (93073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff9c3a70f3e2b4cfbfa8ea0a93d664335a0e7791d3f0fdf0d8d43b89ede3509`  
		Last Modified: Fri, 02 Feb 2024 21:56:06 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb289a0e23f3f9d3ec935d5ff4eca24dfaa3a78d9a6468449497ff969216720`  
		Last Modified: Fri, 02 Feb 2024 21:56:08 GMT  
		Size: 51.4 MB (51354236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064d83a28d09945da34aaaeb608d666c473b7d468972c53594e0801085980a45`  
		Last Modified: Fri, 02 Feb 2024 21:56:07 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b855603001d2faf24213c368123c974608bdfc8a175aca499e6b399c151b773b`  
		Last Modified: Fri, 02 Feb 2024 21:56:08 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087fdfa38134e324728506fd940b65f85398041efb2fbad4357671917de66132`  
		Last Modified: Sat, 03 Feb 2024 12:32:47 GMT  
		Size: 5.2 MB (5235896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-git` - unknown; unknown

```console
$ docker pull docker@sha256:21cf0fc3600d22b65471a7f89c223672314849a252db828be7971f64680cec2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.3 KB (757336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae201c22bc4debe93f6557e6100434ea5b1316db3e913f20a3b7e9855b044b53`

```dockerfile
```

-	Layers:
	-	`sha256:e16ba0b237b980d2d90a95fac2652ea7b85f1f5a30d7143d5e6508f59dc781b4`  
		Last Modified: Sat, 03 Feb 2024 12:32:47 GMT  
		Size: 746.0 KB (745962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40875feee2163ffa9fdc6ff5b426fc1fd046c80053bd3cf4b7c6eccf0ad8bed7`  
		Last Modified: Sat, 03 Feb 2024 12:32:46 GMT  
		Size: 11.4 KB (11374 bytes)  
		MIME: application/vnd.in-toto+json

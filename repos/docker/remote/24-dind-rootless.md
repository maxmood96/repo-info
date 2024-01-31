## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:36252ee1a25e930fa77a4df383e20a47789e870a599714a656e22a82050c16de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:2b894fdca7b13200ddda23bdfe6bb1c5c5324652bcd7eafc210fc345b6ab4a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140777317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c895b8c95629c54caaf3306d84b0a5fe5bb6b6b66764c6fd4f2d10eef95ad4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 00:04:16 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Fri, 26 Jan 2024 00:04:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_VERSION=24.0.8
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.4
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-x86_64'; 			sha256='b506272a7f34ea056e36ba23e83593c491fd8419b0ed30ecacc42fe2eee8c964'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv6'; 			sha256='4b7ca7873d92c33603075ed9dec53a4b7573964eb09e86a3a3e4ded6f88cae1d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv7'; 			sha256='122d3220a3a7fe4d9a02fd9cbe6c342d0edc8494b4531787f3da6f85a5f85983'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-aarch64'; 			sha256='cf59a08baa32a5c8684550b836fb773e7a61a5a355a4a155d848805912244278'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-ppc64le'; 			sha256='3f16bb37487d154b2c4cff1969f7333dfc905bbd1466fcc8f10312dd3fc3f546'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-riscv64'; 			sha256='0f115f2c8a356e931524f0e182e11b0a32cd7f9af19ffecf96b59bba179d225f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-s390x'; 			sha256='ced7587be61c6c18790d4bdeab9cbace6493523ce4196417ef69d326058d3ac5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 Jan 2024 00:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
CMD ["sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
VOLUME [/var/lib/docker]
# Fri, 26 Jan 2024 00:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 26 Jan 2024 00:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
CMD []
# Fri, 26 Jan 2024 00:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 26 Jan 2024 00:04:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db5a4f146e2df1f17a2c0db7ffd672b18d1750d31c7e58e352a6536d4b7ad52`  
		Last Modified: Tue, 30 Jan 2024 22:51:14 GMT  
		Size: 2.0 MB (2018457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248ec8ed73b325a9cff9ec3c5bbd2c249065ee96053dfc3beafb911ef652a195`  
		Last Modified: Tue, 30 Jan 2024 22:51:14 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aed6b72066db35b8929c11c552f9e827431de2b2de62b4384a1eaed88221787`  
		Last Modified: Tue, 30 Jan 2024 22:51:14 GMT  
		Size: 16.4 MB (16409719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908927dc97522b6d63aaaf9953c4095be9b24a1d080edb1ada9124d56bf41ad`  
		Last Modified: Tue, 30 Jan 2024 22:51:14 GMT  
		Size: 17.2 MB (17195293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d280e8e81156b63b7306ac0701738e22b333c7a26bdd96ddafb3ec8f607d2a32`  
		Last Modified: Tue, 30 Jan 2024 22:51:16 GMT  
		Size: 18.2 MB (18202352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f6ee5ccb7fa02811eb89d903666095e18e38c42a635369912f9ba0fd11e6eb`  
		Last Modified: Tue, 30 Jan 2024 22:51:15 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4462dfff57f9ac45d562ae18d1ca53fef4918ae18e003d21ebf960b3ade6f94`  
		Last Modified: Tue, 30 Jan 2024 22:51:15 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a474f84a4abb535fa3a05ee5a59bff31a53d0857d4d53bab82a9f2f3684c4c7c`  
		Last Modified: Tue, 30 Jan 2024 22:51:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb764fbe61245e3574f7dcecbcd507c2bbeaec977fd5b53dd90bb1eb0071296`  
		Last Modified: Tue, 30 Jan 2024 23:51:07 GMT  
		Size: 7.1 MB (7068045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145706c849babe97aaffa0604739299c97d39419215568aa29255bdd83ef6a8b`  
		Last Modified: Tue, 30 Jan 2024 23:51:06 GMT  
		Size: 83.6 KB (83645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533c58802323bbadc41a7a3f07e62537c0520e532bac6c1d99c719e0e7dcf434`  
		Last Modified: Tue, 30 Jan 2024 23:51:06 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd5ad942204b1c752642e7b686af12f948f2da8905ca36cf04e8066bfe65270`  
		Last Modified: Tue, 30 Jan 2024 23:51:08 GMT  
		Size: 54.7 MB (54730901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064eb5baf1167f0bf81369c3dae7c84e05544dd026963e7c5d8f6ca053c8378`  
		Last Modified: Tue, 30 Jan 2024 23:51:07 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26298d2ca15d850dbd6e0b384af7f1cde1790376820dad35f595a2eab64933fb`  
		Last Modified: Tue, 30 Jan 2024 23:51:07 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43188831101cc73d0d740ea695e57ab84e3c6930b54d7ef2c923639113075bb`  
		Last Modified: Wed, 31 Jan 2024 00:49:21 GMT  
		Size: 974.0 KB (974048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681286123e68d0d7e2e624346fbdfb6279f33d43f652354793a2b6e19f0cb41b`  
		Last Modified: Wed, 31 Jan 2024 00:49:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29082af7c1eec7db5507d3ba0987f898221d57426d3435cfec3c37e12430796b`  
		Last Modified: Wed, 31 Jan 2024 00:49:21 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b809d14aa9f336b078c8249f1854c70fd85798ed7c543e76ed681174a6d59458`  
		Last Modified: Wed, 31 Jan 2024 00:49:21 GMT  
		Size: 20.7 MB (20676179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc9b29519422acd6ab2a57390671ec46dd338aca0df55ea327491976bc47fd5`  
		Last Modified: Wed, 31 Jan 2024 00:49:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:9ec3f3ed80b5f6c0a79f10cb8af4484eae28ec84eb21e92b5aeb62881ee73f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.0 KB (776963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2061c8757306dd2c32e4c343d8bf999bfb2c23d24cb7629acfffb6cebaf9569`

```dockerfile
```

-	Layers:
	-	`sha256:c1b77455910ea798c7fbae87972913d02d65c1eb71de403c4e12842d667136e7`  
		Last Modified: Wed, 31 Jan 2024 00:49:20 GMT  
		Size: 744.0 KB (744026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986e03548bc34b2312a13d985452d1d390ca28f29251a8c2cc91c7684d51ef4e`  
		Last Modified: Wed, 31 Jan 2024 00:49:21 GMT  
		Size: 32.9 KB (32937 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f02c32c7e2ed2ebd916a481209e58147b8b9d86d6e83d26497f81ba367aad0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134198007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55184e2fe549bd756992908f5c7cb3c24c14d210238e78f1284b4ed986a00f6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 00:04:16 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 00:04:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_VERSION=24.0.8
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.4
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-x86_64'; 			sha256='b506272a7f34ea056e36ba23e83593c491fd8419b0ed30ecacc42fe2eee8c964'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv6'; 			sha256='4b7ca7873d92c33603075ed9dec53a4b7573964eb09e86a3a3e4ded6f88cae1d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv7'; 			sha256='122d3220a3a7fe4d9a02fd9cbe6c342d0edc8494b4531787f3da6f85a5f85983'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-aarch64'; 			sha256='cf59a08baa32a5c8684550b836fb773e7a61a5a355a4a155d848805912244278'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-ppc64le'; 			sha256='3f16bb37487d154b2c4cff1969f7333dfc905bbd1466fcc8f10312dd3fc3f546'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-riscv64'; 			sha256='0f115f2c8a356e931524f0e182e11b0a32cd7f9af19ffecf96b59bba179d225f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-s390x'; 			sha256='ced7587be61c6c18790d4bdeab9cbace6493523ce4196417ef69d326058d3ac5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 Jan 2024 00:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
CMD ["sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
VOLUME [/var/lib/docker]
# Fri, 26 Jan 2024 00:04:16 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 26 Jan 2024 00:04:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 26 Jan 2024 00:04:16 GMT
CMD []
# Fri, 26 Jan 2024 00:04:16 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.8.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 26 Jan 2024 00:04:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 26 Jan 2024 00:04:16 GMT
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
	-	`sha256:28a7456c7e2e48e3b9172a7ee04cae83fc6b78718d7a8a4a100b97918becfa11`  
		Last Modified: Sat, 27 Jan 2024 17:52:07 GMT  
		Size: 15.5 MB (15461810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18caa195548a3e53f2628e67ea956d63cda5fde48722c22050affc79ec0df56d`  
		Last Modified: Sat, 27 Jan 2024 17:52:06 GMT  
		Size: 15.6 MB (15640600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a151f5451bdb87b23c5abaadadd5829f59ebc94786efba38b5b3d68580031292`  
		Last Modified: Wed, 31 Jan 2024 02:02:48 GMT  
		Size: 16.6 MB (16631366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5a631ed90b271f319528785ca7d4f53ef6f6d6f4b337c87b3f39f8543ed308`  
		Last Modified: Wed, 31 Jan 2024 02:02:47 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70fd66672fe829e203cd2df66e66610c165deea60e2b1c0499d8837c4de35cd`  
		Last Modified: Wed, 31 Jan 2024 02:02:47 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55481dd89fc548546ad551245ad67bd9ce1bd23a820770803027a076c870d4b`  
		Last Modified: Wed, 31 Jan 2024 02:02:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ede2df8a8978d98f53b93ab2377904c57656c8a3e85ba86509239e4703a501`  
		Last Modified: Wed, 31 Jan 2024 04:20:24 GMT  
		Size: 7.4 MB (7428517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14614c618f2c9bf69bb35b2e53a007682cc0d16588ffe3db724c3226c14c088a`  
		Last Modified: Wed, 31 Jan 2024 04:20:23 GMT  
		Size: 93.1 KB (93069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6ca833928550180519aa63032e4de4d82297e3d796db1bd1a981897a1f59ca`  
		Last Modified: Wed, 31 Jan 2024 04:20:23 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107907fed25aff9122158b89c59dffb8c9f5e69635214c8e82b185b4a521ade9`  
		Last Modified: Wed, 31 Jan 2024 04:20:25 GMT  
		Size: 50.1 MB (50072933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dde87a084bc1ed6d311c6f01f7106e69a5b99a2f903a640d9f3ed22462c35c`  
		Last Modified: Wed, 31 Jan 2024 04:20:24 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebeb40f71905f8b3c834bc0deb0c280678f7ed4300845f730bfeaf94c41bb92`  
		Last Modified: Wed, 31 Jan 2024 04:20:25 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176c87f19a419104cb183394e669f752fc0f57a8915b8b74cb1f3835fa6f8725`  
		Last Modified: Wed, 31 Jan 2024 05:30:06 GMT  
		Size: 1.0 MB (1016233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748942d08150c5529870c1e9218efc950c4cb89c194f81795f62883dad67ec72`  
		Last Modified: Wed, 31 Jan 2024 05:30:06 GMT  
		Size: 117.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44652630329daf52173acdb5dcb743412922393ce53baa8b35a2282a7f290867`  
		Last Modified: Wed, 31 Jan 2024 05:30:05 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ab33b0e981d2505c9479a84533174ba5463a92bc4410bc520439116a2160b4`  
		Last Modified: Wed, 31 Jan 2024 05:30:07 GMT  
		Size: 22.5 MB (22476107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fc3c3bb220dbcbdba1cc973b209e1c009f7cad453978071602f392c8241527`  
		Last Modified: Wed, 31 Jan 2024 05:30:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1851bffb558a8b4c200e882480cd97c677bf6cf0dbcee039a7a53937e4c49289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.0 KB (777033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2922c320be2280a91c90e566003f44d6ca9c9676073ec3cda9f1545357b1a3`

```dockerfile
```

-	Layers:
	-	`sha256:2bc4892232a3278c544534dee4c7943cc0d4ed55a0c86ad178ae00044d7975b2`  
		Last Modified: Wed, 31 Jan 2024 05:30:05 GMT  
		Size: 744.0 KB (744035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5c4a36b01ec3a4182309540b2958bb1dcdf54c61bf11e82922470a7a26a3e8`  
		Last Modified: Wed, 31 Jan 2024 05:30:05 GMT  
		Size: 33.0 KB (32998 bytes)  
		MIME: application/vnd.in-toto+json

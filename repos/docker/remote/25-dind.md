## `docker:25-dind`

```console
$ docker pull docker@sha256:c5a417e6561a299f72dddbc013f8ebc81d5a5e7112a994f5f9cc25d7057b017c
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

### `docker:25-dind` - linux; amd64

```console
$ docker pull docker@sha256:67664f7a0f15726cc976c000b3d2784028660c97e237b16a896aa35d37c30f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120514304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cdfe2e8f6571332dfc7894b743fa3189b1bdea4b1dc44e4019d3a3eda26fa2d`
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
ENV DOCKER_COMPOSE_VERSION=2.24.4
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-x86_64'; 			sha256='b506272a7f34ea056e36ba23e83593c491fd8419b0ed30ecacc42fe2eee8c964'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv6'; 			sha256='4b7ca7873d92c33603075ed9dec53a4b7573964eb09e86a3a3e4ded6f88cae1d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv7'; 			sha256='122d3220a3a7fe4d9a02fd9cbe6c342d0edc8494b4531787f3da6f85a5f85983'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-aarch64'; 			sha256='cf59a08baa32a5c8684550b836fb773e7a61a5a355a4a155d848805912244278'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-ppc64le'; 			sha256='3f16bb37487d154b2c4cff1969f7333dfc905bbd1466fcc8f10312dd3fc3f546'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-riscv64'; 			sha256='0f115f2c8a356e931524f0e182e11b0a32cd7f9af19ffecf96b59bba179d225f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-s390x'; 			sha256='ced7587be61c6c18790d4bdeab9cbace6493523ce4196417ef69d326058d3ac5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48a116699ba1fe77921e9ab9fef2dc65016ac2e483b07f03921526b8a0fcf79`  
		Last Modified: Tue, 30 Jan 2024 22:51:20 GMT  
		Size: 2.0 MB (2018473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd9561ee09aa7423609ac837068a53ad4a8fd35b8b6d51528d78cb126eb3b07`  
		Last Modified: Tue, 30 Jan 2024 22:51:19 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dc1292823582d19d9bc523915a590652c16d3bedc6099b345ec38efd77e6a0`  
		Last Modified: Tue, 30 Jan 2024 22:51:20 GMT  
		Size: 16.9 MB (16894259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23a00be1976186eef218bb9b79ab99203e0c5b235c1b49e77f3ac3264793d78`  
		Last Modified: Tue, 30 Jan 2024 22:51:20 GMT  
		Size: 17.2 MB (17195293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d49cdf5732fc93fbea227838e14f9772a369a669592554ca37cf4695be03d`  
		Last Modified: Tue, 30 Jan 2024 22:51:22 GMT  
		Size: 18.2 MB (18202350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6735844810a03df9d76e5aa58d3df2f1c56f6c208093eba5f88e5806f1cda04`  
		Last Modified: Tue, 30 Jan 2024 22:51:21 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49704df22e8621ca86fd75cb61b8f23ee280754df0048a7bf46cd8b96ec2551f`  
		Last Modified: Tue, 30 Jan 2024 22:51:22 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5f50d82ecbeeeea34901bdac4b25948f5f7146f2842d8a7aeb9a730459567`  
		Last Modified: Tue, 30 Jan 2024 22:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6080ddf7a4e419392acc6dbf9a50da4eb37b3cf92202e0e63a70b02f2e189734`  
		Last Modified: Tue, 30 Jan 2024 23:51:08 GMT  
		Size: 7.1 MB (7068044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361b62980a429fc2c236d816d738bf5ed3e8714fa82c03a977926cd518edb591`  
		Last Modified: Tue, 30 Jan 2024 23:51:08 GMT  
		Size: 83.6 KB (83643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fc4f759a829ef8a777e9656b22e3d46b3b2868651832d8771bac1359c86b00`  
		Last Modified: Tue, 30 Jan 2024 23:51:08 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947f26f21b826c2b15adae7cd3e71807bf15e9e0fd9598c70c143ddc83526e93`  
		Last Modified: Tue, 30 Jan 2024 23:51:10 GMT  
		Size: 55.6 MB (55635196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf5330aa9acb3b54fec384542634ad5e0fbf8178caa9f37f25184cbf1ac7788`  
		Last Modified: Tue, 30 Jan 2024 23:51:09 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1e62baa25c29eced2b0d6a8103a493a5902968a8aaeeaa0070d5feea4c9e63`  
		Last Modified: Tue, 30 Jan 2024 23:51:09 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind` - unknown; unknown

```console
$ docker pull docker@sha256:48addc6dec8a7a6a9ba64ca7d69511009eb52f3c4d7e093cb6046b7baf4c259f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.9 KB (730927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512dfd50d71f9d030c34812ec394f3144f71f84e7b9d0150ca9ce7401936573b`

```dockerfile
```

-	Layers:
	-	`sha256:d12088fc016ba25c2d8a4ecca524dfecb8f3bdc0b7de884bc41bef776eee0eec`  
		Last Modified: Tue, 30 Jan 2024 23:51:07 GMT  
		Size: 693.9 KB (693944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6070b9a632cc9c7f781492cdf2fa1f3254b10fcf7ad0125094bea015b2fe2bf3`  
		Last Modified: Tue, 30 Jan 2024 23:51:07 GMT  
		Size: 37.0 KB (36983 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-dind` - linux; arm variant v6

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

### `docker:25-dind` - unknown; unknown

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

### `docker:25-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:566faeebd81d10d2e19b29ca9475f37a1cc967d172c91e33f7594fa29e760062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112086383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4db158eb493c1f3b5568b3e957d85a162b43ea31ad59f36593415ccac9adb0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 24 Jan 2024 12:05:09 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
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
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcc37869d996703b2877f776d94ee24bd228d5baae5c13562b64534676ed8a9`  
		Last Modified: Sat, 27 Jan 2024 15:37:05 GMT  
		Size: 1.9 MB (1896148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf19ffb9edbb4cb5aef681d145a6973e8f789058991e0a84456aff999e6e85`  
		Last Modified: Sat, 27 Jan 2024 15:37:05 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b895a9dd8a21cc28710e5523b0eb56b43e5faa0b40d20d79dda83619194f1d90`  
		Last Modified: Sat, 27 Jan 2024 15:37:06 GMT  
		Size: 15.3 MB (15267848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8952ee4ae143efa122dd8a052cfa8fd6d374f4b32f2ef4dfa66e136354f2de43`  
		Last Modified: Sat, 27 Jan 2024 15:37:06 GMT  
		Size: 16.1 MB (16084083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1730bc7ecb997da0d798633674b0fd703713df5c0d2471ce736881fd31a7f5`  
		Last Modified: Sat, 27 Jan 2024 15:37:07 GMT  
		Size: 17.2 MB (17167110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255d330b03145f4ea17fa8a3a2021a680a9c2958667e81113c525518b8cf7a8`  
		Last Modified: Sat, 27 Jan 2024 15:37:06 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bae639f812542ddfc611b695f844f2158592015526f8ed7af8ca427d909054`  
		Last Modified: Sat, 27 Jan 2024 15:37:07 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f19cd7fb7b1bffa68f172e2c6eb96f9410a3b1c8d199c38c624b9eb7f201576`  
		Last Modified: Sat, 27 Jan 2024 15:37:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1380c84ea7c4f508c45f0e542a73dee24570994b4cfcf16bb125e6b234fac4de`  
		Last Modified: Sat, 27 Jan 2024 20:45:06 GMT  
		Size: 6.6 MB (6649814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8e0706801c031fee5a5bf24f679748c1409e1b4cacb125abdd8c57aa16b13`  
		Last Modified: Sat, 27 Jan 2024 20:45:06 GMT  
		Size: 78.9 KB (78891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d87056d1c6f3421047672156e4714f0314a6b872956018f7155ce799048f7d4`  
		Last Modified: Sat, 27 Jan 2024 20:45:06 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16702f683589f9fc8974789c58e1342ce1cd0e648cc48377d23f152601ae02`  
		Last Modified: Sat, 27 Jan 2024 20:45:08 GMT  
		Size: 52.0 MB (52015258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51626cfd55332f181b866bed6c1e54be06b369a36f37285bf234d34ef838e9b7`  
		Last Modified: Sat, 27 Jan 2024 20:45:07 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96eb2e189dcb3a616b74952cfcc2df97d9e4a50ab4371818a07d4e43e05706cb`  
		Last Modified: Sat, 27 Jan 2024 20:45:07 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind` - unknown; unknown

```console
$ docker pull docker@sha256:155f1b88c4f603690a4e51dec9027d06fd0095b8b698029b0323cfef574f91d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.2 KB (731235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66983ae403085c9c7ee92797d5e2f73d466950b6f75c7b4dd33b322b5582d93d`

```dockerfile
```

-	Layers:
	-	`sha256:8280c97ed305ca4374efbd8b40a9e57503d5a9365c5e3797f0af4fc575727521`  
		Last Modified: Sat, 27 Jan 2024 20:45:06 GMT  
		Size: 694.0 KB (694028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cba3c6299e9b592a83ba645a2db3e5070de7ade73cb580ddba72a644a09688b`  
		Last Modified: Sat, 27 Jan 2024 20:45:05 GMT  
		Size: 37.2 KB (37207 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:91710ea9c7d32e4b2571d4281e0d0075f56368bdb711d0eff099a40e80f7825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112412180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9e3d882cb0fab9856be17172cf11b83ac453f2c16e390ab6f83212f3edbe58`
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
ENV DOCKER_COMPOSE_VERSION=2.24.4
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-x86_64'; 			sha256='b506272a7f34ea056e36ba23e83593c491fd8419b0ed30ecacc42fe2eee8c964'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv6'; 			sha256='4b7ca7873d92c33603075ed9dec53a4b7573964eb09e86a3a3e4ded6f88cae1d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-armv7'; 			sha256='122d3220a3a7fe4d9a02fd9cbe6c342d0edc8494b4531787f3da6f85a5f85983'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-aarch64'; 			sha256='cf59a08baa32a5c8684550b836fb773e7a61a5a355a4a155d848805912244278'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-ppc64le'; 			sha256='3f16bb37487d154b2c4cff1969f7333dfc905bbd1466fcc8f10312dd3fc3f546'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-riscv64'; 			sha256='0f115f2c8a356e931524f0e182e11b0a32cd7f9af19ffecf96b59bba179d225f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.4/docker-compose-linux-s390x'; 			sha256='ced7587be61c6c18790d4bdeab9cbace6493523ce4196417ef69d326058d3ac5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:5a0da380a768694cc743dac53a0f6c636c40f8aa43a19ecb562738a5c57f6675`  
		Last Modified: Wed, 31 Jan 2024 01:19:04 GMT  
		Size: 16.6 MB (16631362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3364e0c80a68603d41732545cd5cb7c7d16a0e7bb240704b9b0c561074e4f5`  
		Last Modified: Wed, 31 Jan 2024 01:19:03 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d397e39bdd498243dbd9db0e1a6cc8958951e09f69cc781d6667ba0e7674a5b`  
		Last Modified: Wed, 31 Jan 2024 01:19:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058c8bc732080d11a5f1a40557e4fd40bc56652c66ad7a526677ec41b14a90ca`  
		Last Modified: Wed, 31 Jan 2024 01:19:03 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f992dd6a8e29fd8964e63307602027c098582ab3217b2c2a5be1dcd58f430f`  
		Last Modified: Wed, 31 Jan 2024 03:51:13 GMT  
		Size: 7.4 MB (7428552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f02797638634962ad874922598136f85a64209236084971dcc0f396893ab6b`  
		Last Modified: Wed, 31 Jan 2024 03:51:12 GMT  
		Size: 93.1 KB (93073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccc0a04b9555cc301e201f935e8bccfba3639f893a522cb0712a853cdffbbc7`  
		Last Modified: Wed, 31 Jan 2024 03:51:12 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124d7d852822e8a3bd01b7f1e3f08cdeab760e869298207e258b563305ed170d`  
		Last Modified: Wed, 31 Jan 2024 03:51:14 GMT  
		Size: 51.3 MB (51341262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9578c7c454c5c47ea5f658a55afa771b6cd9d14cd3117d44132f9d9ac67e507`  
		Last Modified: Wed, 31 Jan 2024 03:51:13 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ff999be3f2eb473c985bb6a89b1d7cb9d5e48aec53f8691a84a555a0c0f15e`  
		Last Modified: Wed, 31 Jan 2024 03:51:14 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind` - unknown; unknown

```console
$ docker pull docker@sha256:681bfde590e987aa4c9f1403490393e32dd3bfca84861f525d692614ae9d3ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.0 KB (731026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8515fc14031cf95cdffc1f8069074268883ef88d364cba73bab2221910d4c33d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0de65c2b3df1f1ca5bf110d4f3ea3673b693530ed332558f2b293d8c393520`  
		Last Modified: Wed, 31 Jan 2024 03:51:12 GMT  
		Size: 694.0 KB (693967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a175048a91e86e4a73c9af7bcad1de578785fe7d764d03cc775c55f4cffe454`  
		Last Modified: Wed, 31 Jan 2024 03:51:12 GMT  
		Size: 37.1 KB (37059 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:d25826ad7f4ae09439fc7540a95c3e48602ae8776a55d9d89342009102635d52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c9a0c5324d225909d9c9d84cdae6310df403942501eba0c0ca7259ecb8253bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151798458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadfc139b041cd5981c5ae0cbae9735094a7e9d2f3e01cb56e49d0d42a065901`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 16 May 2024 16:36:41 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Thu, 16 May 2024 16:36:41 GMT
CMD ["/bin/sh"]
# Thu, 16 May 2024 16:36:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_VERSION=26.1.3
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 May 2024 16:36:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 May 2024 16:36:41 GMT
CMD ["sh"]
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 May 2024 16:36:41 GMT
VOLUME [/var/lib/docker]
# Thu, 16 May 2024 16:36:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 16 May 2024 16:36:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 16 May 2024 16:36:41 GMT
CMD []
# Thu, 16 May 2024 16:36:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 16 May 2024 16:36:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 16 May 2024 16:36:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cb2a59ced673275c4d194fc0bf5a88d16561a08dc3bf1e300878396a062eb`  
		Last Modified: Wed, 22 May 2024 22:54:40 GMT  
		Size: 2.0 MB (2010472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb247a8f83e747078be96970bd4a0b1550bc53508f29ec882ee2c629ee5c9e95`  
		Last Modified: Wed, 22 May 2024 22:54:39 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32499521033d872bb3ecaec64746bb66e8865da4220597373b6ee8e135138d2`  
		Last Modified: Wed, 22 May 2024 22:54:39 GMT  
		Size: 18.0 MB (18031645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38fd5a68d3448d81e597d18b7ba48addada8c54857f7d350f4f10068200b415`  
		Last Modified: Wed, 22 May 2024 22:54:40 GMT  
		Size: 18.1 MB (18089095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421921fd35be50f14f772e703fd96c5f47727915d87b24d22eeafa897f76d2e7`  
		Last Modified: Wed, 22 May 2024 22:54:40 GMT  
		Size: 18.8 MB (18764679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcd32e1b4bb951b68185e09df7da620b58563f8b93ba02db839bb703d0bd0d6`  
		Last Modified: Wed, 22 May 2024 22:54:40 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6456e0b3931787e86695d10d8725381d2c98ffbda04d774c3a11fd1dfc3bebae`  
		Last Modified: Wed, 22 May 2024 22:54:41 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d97db5952e9161d03e0800789a7ff38f8e585a9c939c108e0c2c925d651b7ad`  
		Last Modified: Wed, 22 May 2024 22:54:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859ef0cd825e91ac58bd364637bc16cb4088d96fd4b2eba3271d949cd30784d6`  
		Last Modified: Wed, 22 May 2024 23:55:24 GMT  
		Size: 12.5 MB (12508612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46152ab1f3a5ea3e6ac21c7709d7a817114cdc2fcb9a094eee9d09b0e29b917`  
		Last Modified: Wed, 22 May 2024 23:55:23 GMT  
		Size: 89.2 KB (89184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b13da4650b450bfee688fdc93bb857be37af6afa7d3327e6ff06133a022e8a`  
		Last Modified: Wed, 22 May 2024 23:55:25 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e2fc653a42dfd584bac41a94de50033fea24391127cdcc68c270e6e1cd5f4d`  
		Last Modified: Wed, 22 May 2024 23:55:25 GMT  
		Size: 56.7 MB (56711330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6858fca25ac09843df6297ab934affcc2ae99449b5d73efc83737777de477344`  
		Last Modified: Wed, 22 May 2024 23:55:24 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95be673f87cbc7c6ab856585c96071d212fd9b8d83350806443fc4a4051eeea`  
		Last Modified: Wed, 22 May 2024 23:55:25 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6912249627e9e89f3ebc1eb6a88843ad8a9e3114851e924b848cf47958451864`  
		Last Modified: Thu, 23 May 2024 00:51:37 GMT  
		Size: 981.0 KB (980956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be6b248424f352c5c1dc4f7f6aedc2551a5a5e537ac40d00c0028edf268be55`  
		Last Modified: Thu, 23 May 2024 00:51:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724f03b58718f814f47ccbde6587ab42b674de68af12e6d946305a3955d56257`  
		Last Modified: Thu, 23 May 2024 00:51:37 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b2bc113de2812f6ad1536e7f281ff53317ee4041bcc656e7c9695714d5f8e2`  
		Last Modified: Thu, 23 May 2024 00:51:38 GMT  
		Size: 21.0 MB (20981096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293593cae5233969d32b18b814a968d512967fb2b5cadd8b92044879c0d294e`  
		Last Modified: Thu, 23 May 2024 00:51:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:54ef0261639b1e7d8c1563cac6c0c12562860a3e80c1e93babf0cdb74f483b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (33041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51bc63e7eaf01736308afe9de1da75a070b00a014c59bdda57e96a4b3cfa11e`

```dockerfile
```

-	Layers:
	-	`sha256:16ea4c7d7056e64b62c7a0f5315b463273351c133c458deb7ac69ee6902b25db`  
		Last Modified: Thu, 23 May 2024 00:51:36 GMT  
		Size: 33.0 KB (33041 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:64289f6e1c1a34c3acff0360d95bbd5355a2672ae3dd625d10466570846d4f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145955171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323338b9cc675bcb133cc25f2c33f73cc5f7392d62d5fa5df3f67f2e58cf404e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 16 May 2024 16:36:41 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Thu, 16 May 2024 16:36:41 GMT
CMD ["/bin/sh"]
# Thu, 16 May 2024 16:36:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_VERSION=26.1.3
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 16 May 2024 16:36:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 May 2024 16:36:41 GMT
CMD ["sh"]
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 16 May 2024 16:36:41 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 May 2024 16:36:41 GMT
VOLUME [/var/lib/docker]
# Thu, 16 May 2024 16:36:41 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 16 May 2024 16:36:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 16 May 2024 16:36:41 GMT
CMD []
# Thu, 16 May 2024 16:36:41 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 16 May 2024 16:36:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 16 May 2024 16:36:41 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 16 May 2024 16:36:41 GMT
USER rootless
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeff538fc611c5175105f9f005c3552426210b835f1716c1b5e1521c54176b7`  
		Last Modified: Thu, 23 May 2024 06:13:27 GMT  
		Size: 2.0 MB (2006606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b49800f10e13b1bd816fa74ace8882c4c7340e84c68b55a44add2715286e4d`  
		Last Modified: Thu, 23 May 2024 06:13:26 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bceab9a87f0f744c442f0fd063f1a00e0351a48d6c4476028febb80586c82`  
		Last Modified: Thu, 23 May 2024 06:13:33 GMT  
		Size: 17.0 MB (16988430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061f435c49b2fa9f18104b78ef3de0960c5e4c93a6a60a60f0425ca393358b49`  
		Last Modified: Thu, 23 May 2024 06:13:27 GMT  
		Size: 16.5 MB (16450822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19b16c332f9523cf5299647fe3decef4a10241a395420fdcf7a62c91eccfd27`  
		Last Modified: Thu, 23 May 2024 06:13:28 GMT  
		Size: 17.1 MB (17134298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eb2e65793799cd32f571ae16f4f26a892bc383c1a452d8c383b178926dad6d`  
		Last Modified: Thu, 23 May 2024 06:13:28 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6846f7d028260698208b6ad0eaea09f5aae1e04c937ea835936fcc0fd22c3164`  
		Last Modified: Thu, 23 May 2024 06:13:28 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673d1bb4a6e79d9eb543938b510283ddc0313aac961761d8e20b4a2a68e80ea1`  
		Last Modified: Thu, 23 May 2024 06:13:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f95161f9fff626fccdded4b382bef457bec167bd0963c9e5d364d7a2cfdc2e2`  
		Last Modified: Thu, 23 May 2024 08:40:59 GMT  
		Size: 13.0 MB (12993421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd13f9fb933cdbe9d678236501e612276cfb92f3d1827641ca529faa0cde1fe`  
		Last Modified: Thu, 23 May 2024 08:40:59 GMT  
		Size: 98.6 KB (98619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e24dd90fbbdcafcf7dc4f16b95252104ee44d8f73a64da7d74b422e78d2adb6`  
		Last Modified: Thu, 23 May 2024 08:40:58 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0421940cb8c54870571840cce95e302cb3e8664847627163dbf16879aff92ff0`  
		Last Modified: Thu, 23 May 2024 08:41:01 GMT  
		Size: 52.3 MB (52318638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30513560a1ac6588fd9a70c4548154a2b4f5d597f84f747a1c305f5c1f38d6ef`  
		Last Modified: Thu, 23 May 2024 08:41:00 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b91ae4e0e1d957deb9ec34789ab83f53cc8a364f736344835a38d567a92af0e`  
		Last Modified: Thu, 23 May 2024 08:41:00 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a91fa8753acdc911fc2856b5c5086ab7d8d01125878ca43ef6fb76f0e8533a9`  
		Last Modified: Thu, 23 May 2024 10:31:13 GMT  
		Size: 1.0 MB (1023057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb9fa5605678db3e04b33371ebff57dee4814b5f9d2f5d9225d346b0d99bf8a`  
		Last Modified: Thu, 23 May 2024 10:31:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4955cd5601f1d723d469d6497343ea7995558346d51f24751c9757f08c7fb9c2`  
		Last Modified: Thu, 23 May 2024 10:31:12 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cd9d6589651907f8dcb0454db9d42e6576f74b29ad52e4872e16da005b7427`  
		Last Modified: Thu, 23 May 2024 10:31:14 GMT  
		Size: 22.8 MB (22845210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5aa9306bec0212f6b6191dc6effcf81b4509c248495c1aa96984630618aafd`  
		Last Modified: Thu, 23 May 2024 10:31:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:187c56f5a613c0a01455fc236836a75dcd42e9bdae7e7c6f26e927332e7bbb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 KB (33103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2318c7e10046765b662dcad424301b19835cd84170c8112848062aa75f7f25b0`

```dockerfile
```

-	Layers:
	-	`sha256:bd614e54a28174841ab40c0b0ddfab7efb5f0a3a8b36b6d0ffa79a81cc432dee`  
		Last Modified: Thu, 23 May 2024 10:31:13 GMT  
		Size: 33.1 KB (33103 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-rc-dind-rootless`

```console
$ docker pull docker@sha256:fe0147385d0008a423b2e0c618136dc891819af080b5365e7c98229bd436ddf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:a86fd011b67d2276abd9e11dd67ad8311e8683c42c9e94401274ae4d1063d211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152533470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032127c17f2509d8fecb47d6c050e8d0d970363840156f03a98a75de59a7cf6d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_VERSION=27.2.0-rc.1
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD ["sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
VOLUME [/var/lib/docker]
# Sat, 17 Aug 2024 05:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD []
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 17 Aug 2024 05:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b826b4df39e8b6818aebd9eb70c4704bb0c97fc2cb464aa28510da90630351`  
		Last Modified: Mon, 19 Aug 2024 18:59:19 GMT  
		Size: 7.9 MB (7872281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ee97e7ed5f9f5b0e8abbbf4bd025bff9b040451692c8c646b6f6acc5a1270`  
		Last Modified: Mon, 19 Aug 2024 18:59:19 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb812271b283b43e9c4f2f97567fef7a516fb56c9711dfc83c2d1542037c468`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 18.3 MB (18318205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b789603700e5b3db4e3d0433d1a05227e1bc914313dace943393a7ec2388f45`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 18.4 MB (18404803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3295e68d9ed551c77c847e1464219797b4f10b538bd1d3ddb7845d83adf451`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 18.8 MB (18825286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9917b18cd48d8e82e1f25127437de1b1c380fffd40cce7476361dfbdc7a73202`  
		Last Modified: Mon, 19 Aug 2024 18:59:20 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6acf233fd00d766253e3e1a75561098dd84c85485a3014718c78820e1c0db6b`  
		Last Modified: Mon, 19 Aug 2024 18:59:21 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7925fadc402ad01d5de8aaaf5e54e7255a07c6bd6a36565c4bec0eaf098f49`  
		Last Modified: Mon, 19 Aug 2024 18:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc7a4c3f0a132618da8945101f28aa00c983f1e220eaef8ce1955db8c6c17f6`  
		Last Modified: Mon, 19 Aug 2024 19:51:41 GMT  
		Size: 6.7 MB (6657655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff410ea08e469d13a338681bc58a857a91f1df4cb8b0d7a5eaf49f42b58b1189`  
		Last Modified: Mon, 19 Aug 2024 19:51:41 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926eca05e9b5ce42c69d450078fc4be1ddde7a779fb6a2d83ee1eb247f949b98`  
		Last Modified: Mon, 19 Aug 2024 19:51:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e98e1e520c556c31993a508a2803b68e7c5111ab28579e4c8c8d34edd24485`  
		Last Modified: Mon, 19 Aug 2024 19:51:43 GMT  
		Size: 56.8 MB (56773082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e2ee841e4f6cd5db0b3769603426e68bff61eac4b47d7c7786248d5483362d`  
		Last Modified: Mon, 19 Aug 2024 19:51:41 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6278100443577417d1716bbc6f10e32139f52c14dc45725b5173d08ffe76c08`  
		Last Modified: Mon, 19 Aug 2024 19:51:41 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b16d14a8f139b0cbf57fda52d8bf47a01c6ffe5c03ec76280abc5c14dd12b3`  
		Last Modified: Mon, 19 Aug 2024 20:57:09 GMT  
		Size: 981.0 KB (980980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5680ace1a124a82230ca6ca0c87f93b0c22a8aaf0bac7bcf46d6a0021cc3af`  
		Last Modified: Mon, 19 Aug 2024 20:57:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363c56430667633e7bbca2c54a43b81255b20d1a1fcc8779783d79d8e9ab083f`  
		Last Modified: Mon, 19 Aug 2024 20:57:09 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051eac94f88e6f085fa8320c8eb5819eee01be245443d70938c9cb10cb72eeb6`  
		Last Modified: Mon, 19 Aug 2024 20:57:10 GMT  
		Size: 21.0 MB (20979758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ce136d14a9dd545df49d8a0b167694e992a77419ed16ab206d1b152b7c5073`  
		Last Modified: Mon, 19 Aug 2024 20:57:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e47ec7c913c6bb2879a60a26d2402e12d0a9ecf85799f7621f61b58d88417b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fba46e07b0ae3000c7dd78f241b67d196c723ec3237c4821de7d3a28e025329`

```dockerfile
```

-	Layers:
	-	`sha256:0eb65c55212e82d7ac83f2bae5f8f99e82e778ceb6a8d7d6d09aec6c97fe70b5`  
		Last Modified: Mon, 19 Aug 2024 20:57:09 GMT  
		Size: 30.3 KB (30332 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b7d3062d45832c393dadd8e426ecd7ce1aec9a0fd2c7c947368117b823fa8a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146688114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e492e482410c7f8b51565ee79de57c41f844a9e9facbfe2433fcb093131d9c8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_VERSION=27.2.0-rc.1
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-amd64'; 			sha256='43e4c928a0be38ab34e206c82957edfdd54f3e7124f1dadd7779591c3acf77ea'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v6'; 			sha256='77678205fbaaead25167cd93b022996d0bafff67deb5ca82b92b25cccb06ad07'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm-v7'; 			sha256='b4f029ed0d4d30c49857bc31f8bec5484b3f6b8104d8d49a187fb6b69fab3d82'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-arm64'; 			sha256='775f1ab64aa0e5d901dcc6ecf6843ec3261f27476873760711aa362b403f61f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-ppc64le'; 			sha256='956b020318ad0ba94f817116792d9da8695ebab38254c9f821a85a3369175f7e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-riscv64'; 			sha256='e90589ff33ad409a40a5e53cde5af4a0f230f0d8f5b6d9af522120a6900222ea'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.linux-s390x'; 			sha256='f2dbf2dc967415e1e1f4398d040d6b5b81e4e27f37df22bd148ea4b18c8ea6eb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD ["sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
VOLUME [/var/lib/docker]
# Sat, 17 Aug 2024 05:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sat, 17 Aug 2024 05:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 17 Aug 2024 05:04:22 GMT
CMD []
# Sat, 17 Aug 2024 05:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 17 Aug 2024 05:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 17 Aug 2024 05:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19dc33df4c8f435b82bd76228e820d17db82bafa51365d6d7ca39f18b0ac35`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 8.0 MB (7981766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc98e249bb1c68fcd6c7af4cd94d4dc840949342f303f3453b89e47b10baac`  
		Last Modified: Mon, 19 Aug 2024 18:59:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b064ad1c39cab9bbd12ce8a44da8ca317ae42aafc3a703eb68481279fac32d9`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 17.3 MB (17264856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36074db9005cb79314791a9d04733048d5cb0703a7ac13b89c26d810045b89d`  
		Last Modified: Mon, 19 Aug 2024 18:59:40 GMT  
		Size: 16.8 MB (16772961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb8b806a016e2bd5e83e137c7787981575ad2ce863d92ce07cee3fc38544c78`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 17.2 MB (17186835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764856852ab1b254b572502db9ed0d8fd601e8e615ae83ba73c5a1e5b592c9ab`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d43f3808e72acbc083572802b4b53a88aa4088c8e2d99825cef40e03c050fd`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12ab67b46ae8edc30d74e102545f60cf7042a2542f02c2b8e7f0a313592f473`  
		Last Modified: Mon, 19 Aug 2024 18:59:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae5fb6ccf4a163f82c494b7b9caf3dd9ad4b865c7923f99e1b9d969dbfbe31`  
		Last Modified: Mon, 19 Aug 2024 19:51:28 GMT  
		Size: 7.0 MB (7034951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9747f9655f8f5a18e1f04c84474e64bf4af06cf9a3b0940811d176fb15124d`  
		Last Modified: Mon, 19 Aug 2024 19:51:28 GMT  
		Size: 98.7 KB (98658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30194908ca2a1d60bacf29c1b2422f4f74e8a5587571fe332a8d909021338c6f`  
		Last Modified: Mon, 19 Aug 2024 19:51:28 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60aee437e11c55a81b75f98d77183616292c4270cd75685ecd019c60661872cb`  
		Last Modified: Mon, 19 Aug 2024 19:51:30 GMT  
		Size: 52.4 MB (52392865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5637ce5921a2d301d958f3e970b359747e220bd4ff8b77d743b67cf35348c91`  
		Last Modified: Mon, 19 Aug 2024 19:51:29 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32651485ff3e08e71cc5b9afa52a8300e9f416bcb44a26e9559b887f4ff0a985`  
		Last Modified: Mon, 19 Aug 2024 19:51:29 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0c3cf21d79d7eb44a3f2a6e7625e4067902211dc0937dcbb50b9195babff01`  
		Last Modified: Mon, 19 Aug 2024 20:57:05 GMT  
		Size: 1.0 MB (1023121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6099d39f19f8493ccc63aee3fbfc44c3763b90926bcdb5596602abd7c4926e87`  
		Last Modified: Mon, 19 Aug 2024 20:57:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6906666b8239d3de1bf21bb23dbb6a98f258eee1c1bf7dd7909eb33a67b04bc4`  
		Last Modified: Mon, 19 Aug 2024 20:57:04 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3351d1dcdad4b80cdfd7d1f5c53cc9b0232d11b3a5439cc777dec2e339e1a041`  
		Last Modified: Mon, 19 Aug 2024 20:57:05 GMT  
		Size: 22.8 MB (22835871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfab57dd86a8ffd296e08cfbbcffb748b3c6f2c1d083ff7a909a946e3ad9b9d0`  
		Last Modified: Mon, 19 Aug 2024 20:57:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2fc94ad2495befa7b8bbaebb443f6b2fd2c79df800f1363d7f07497f52d3d419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e598e87260c086bdb0085fbc5d95dfbea4e08a37f37f932eafa79162b1a82ef7`

```dockerfile
```

-	Layers:
	-	`sha256:40c381e08f3582a33f8225ffcc5fb929c6ab34f535b5c16e655523fa54791ad5`  
		Last Modified: Mon, 19 Aug 2024 20:57:04 GMT  
		Size: 30.7 KB (30746 bytes)  
		MIME: application/vnd.in-toto+json

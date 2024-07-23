## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:2c492c01a01eb2b9ef8db3302fdddbad0f5e87672d948f72fddc57d093cfdc2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:f20339a9dc038e9a73a54354732a3e5b1ea8f3751e0dea3f8a10d26f0d1f4975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148275734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291e2d87f92b1353a4de45c6fc7607753095b94df28496c0a7eaf148c3a949e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 01 Feb 2024 16:06:26 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["/bin/sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_VERSION=24.0.9
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD []
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3c120a1b8ff01befb72427f3b4ecd2367902a71201c5e7d95aac8d70e7e33b`  
		Last Modified: Mon, 22 Jul 2024 23:03:19 GMT  
		Size: 7.9 MB (7869168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7211833d84ae182809138c7242a1968a60eee9441664a20821ffa7bc009fd69a`  
		Last Modified: Mon, 22 Jul 2024 23:03:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931c8f5bbd9a87e398eb949f2c899ef96041a017e17274e5cab53817a9b92f92`  
		Last Modified: Mon, 22 Jul 2024 23:03:19 GMT  
		Size: 16.4 MB (16410669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12cbe4de608bb8add4356a8208a07652de59ddc9fbfea1fb679f1d651e85a2`  
		Last Modified: Mon, 22 Jul 2024 23:03:19 GMT  
		Size: 18.4 MB (18404718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834835de77d053e16631676c07baa8a882133783bce35a97a3c58ebde0768f50`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 18.8 MB (18816952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a701b4a8954eea579cdbdcd94d5f0064db3d43ebcc6d7198cea7d8e8b4cc46`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d598586eadbee8edb2b348ef6d1233ed7b6f6ecf4fd651a6299061ae5fbb12b`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bde271ffeb56dbaeb65c8c3f906d0c79cf41a848b2fc482287b88efefa9f885`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27db082605b0cdfc32ecc028d6da4270ad1a802d317c1242338eb24e13429a6f`  
		Last Modified: Tue, 23 Jul 2024 00:06:51 GMT  
		Size: 6.7 MB (6655112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd981c1973ac9763c260627c6c3bd5fac6241e31354bb7b758bea55dbb6cb3f`  
		Last Modified: Tue, 23 Jul 2024 00:06:51 GMT  
		Size: 89.2 KB (89206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a8717c09af99e8a8ad587e3efa158f8a0ef7dce8c4a40ede17f5b813fcb916`  
		Last Modified: Tue, 23 Jul 2024 00:06:51 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9610c0d5da85fc2172ebb7e5e8bd338ca5874f89203ba0c3dd81d2973902fdc`  
		Last Modified: Tue, 23 Jul 2024 00:06:51 GMT  
		Size: 54.7 MB (54740550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0907765db40e2e311934644d0d908835e6cf75f727bd4691b853d52d5f77b406`  
		Last Modified: Tue, 23 Jul 2024 00:06:51 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc81bb4f1c1beae0b82a23661b6381cf65a2baf3de3f68b05e76dac80681d86`  
		Last Modified: Tue, 23 Jul 2024 00:06:52 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97894f376dff8b88638241769b673602bb9d24ddd4f3d3faef21e1938e7c3cc`  
		Last Modified: Tue, 23 Jul 2024 00:58:58 GMT  
		Size: 981.0 KB (980982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a52a0935f9c1468c938e5952ce06c5719797a74c8b96cfc12ff3ae4b2a0c4c`  
		Last Modified: Tue, 23 Jul 2024 00:58:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9ad6e4fa509efda3fe643f08e7b646b5abcd01cf654788205e0b44428d84a7`  
		Last Modified: Tue, 23 Jul 2024 00:58:58 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c81918f2a051f8cd1b54f9af4220b02468172f8ba00f4e4f712c6391a28a84`  
		Last Modified: Tue, 23 Jul 2024 00:58:59 GMT  
		Size: 20.7 MB (20676184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93630e4c1ff7e61cb1a64aad953f84b1f234687b93fa1e4f725b2b23af9bd3ad`  
		Last Modified: Tue, 23 Jul 2024 00:58:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:877b64a488842eb2650914323c65178cb9f044a75e3aa4facea3fa8eff3b9d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94fcdd90e90e3bc336518c9200258c322f7d6171f79344c5882ded08a18fb9f`

```dockerfile
```

-	Layers:
	-	`sha256:da14b4f0370f92f9dc41a19694152e3601df4b8044daa0c5543dc5c453ff9237`  
		Last Modified: Tue, 23 Jul 2024 00:58:57 GMT  
		Size: 30.3 KB (30268 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ced4fe8600951afcec12f6d5330db8f4389b6175b5d8b00a44ab3f4cb531beb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (145008032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f556e1e7196cc2b9cf1895c02736f56c9da4cbdaab630f2fbb65e421fff2160`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 01 Feb 2024 16:06:26 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["/bin/sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_VERSION=24.0.9
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD []
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5d3253e0ef3e94e260674fe19ae1bd8c5014efd17181db97320f4a346f3a28`  
		Last Modified: Fri, 19 Jul 2024 18:00:37 GMT  
		Size: 8.0 MB (7974733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4125e131df37b845c0af771bb895ba7bdd0762a3c3a38a7c202e894736663e3`  
		Last Modified: Fri, 19 Jul 2024 18:00:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3963822fc4599ff7041cd29e0fb4fb33f3f6c7f449abf689f0668737be8f61`  
		Last Modified: Fri, 19 Jul 2024 18:01:02 GMT  
		Size: 15.5 MB (15459136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755e7efc11c8a974f8c6cb6a7af06ec5874e1505ebd418489ab912eae3be1a16`  
		Last Modified: Fri, 19 Jul 2024 18:01:02 GMT  
		Size: 16.8 MB (16772749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f5889c4c9f9817b9348cd49e90cd7dcbe75d188f2a58e6972ac4ff925adad8`  
		Last Modified: Fri, 19 Jul 2024 18:01:02 GMT  
		Size: 17.2 MB (17176044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188eb67a607ab2c2e0a5c253d4e86182c9cd02c1dc55be445f3c40192a0aa5ce`  
		Last Modified: Fri, 19 Jul 2024 18:01:02 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249ec391e552895c46b7dd9edd2ce9b7179c9888ee4089ae45a4524da520ce58`  
		Last Modified: Fri, 19 Jul 2024 18:01:03 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886710ee42ea176ea97f5723541276dd34c410bd7812eab996f44c58252e2bb6`  
		Last Modified: Fri, 19 Jul 2024 18:01:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9778ac3ffe7ac28ac67f9d04fd9844c7559dff77f9fa61922a1acaf5df5ab02`  
		Last Modified: Sat, 20 Jul 2024 00:50:46 GMT  
		Size: 9.9 MB (9853099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632144377c6751599cc6b5d30a204e5b1cae58af6af09a60ed7a92d7d991db7b`  
		Last Modified: Sat, 20 Jul 2024 00:50:46 GMT  
		Size: 98.7 KB (98701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295fc66907689bc09955d06bb1df995e7e6b590255ec1e274da6bdf41d1147e0`  
		Last Modified: Sat, 20 Jul 2024 00:50:46 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0172c31c6868da3051e3d4c2636d5409116334d9a2fda01b41ab74e06fac4c5b`  
		Last Modified: Sat, 20 Jul 2024 00:50:48 GMT  
		Size: 50.1 MB (50076181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b3c19f8e9949e31f6fe1fc6b5d3a9281ea2c70d0c650d4992c68531c56cdb9`  
		Last Modified: Sat, 20 Jul 2024 00:50:47 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1df4ad76b707e5c626b9fed275c8878a0decbbfbb8bede5d42e463380107296`  
		Last Modified: Sat, 20 Jul 2024 00:50:47 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6192d371d2a16245b9cb6c4d562a01d014b5597024c74a42f789683545b33ac5`  
		Last Modified: Sat, 20 Jul 2024 01:57:01 GMT  
		Size: 1.0 MB (1023191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc661ae577d0cd66de1419e4dc07e1c22476026f943edbcae79fe3eb8f4345f0`  
		Last Modified: Sat, 20 Jul 2024 01:57:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e19dc836779cf47b37f4a686cf648651d301424cb781a48dfa2fe40a01a421`  
		Last Modified: Sat, 20 Jul 2024 01:57:01 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff2b4f13d610d64b9a92226dc448b584fb55115d186e01787cff0ef184697bf`  
		Last Modified: Sat, 20 Jul 2024 01:57:02 GMT  
		Size: 22.5 MB (22476087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da394abfc0772da6ed1255a969f77ba8a6c231771629bc27fcde772e7ac0b44b`  
		Last Modified: Sat, 20 Jul 2024 01:57:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2ba4f92fb58fdfc6b157267d4e4d623e9d2878480d35eead021090e040bf807d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd9ec1efbd063cc590875cdf836cff84d2ed7b374f2bcce38ff6405ae2fd28f`

```dockerfile
```

-	Layers:
	-	`sha256:89e76c99cf15266a2bac90f91ca901b013ca9a096b2b5b8a5b6787e94a3461ef`  
		Last Modified: Sat, 20 Jul 2024 01:57:00 GMT  
		Size: 30.7 KB (30682 bytes)  
		MIME: application/vnd.in-toto+json

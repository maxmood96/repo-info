## `docker:25-dind-rootless`

```console
$ docker pull docker@sha256:c212b1d8be90a82eb8903d0e6d0864b351b64e1086e3d7ea4db4beb48bfc8f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:25-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:df6bd56a21297e86a5e227eccc8dfbb4529842f3ef00d6f0e3b8f39786678de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149999573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52eb41a9e420aff7296aeead73f4ff4d970becc3fa0d90798768f5caf1a0dc9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 19 Mar 2024 21:53:23 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 19 Mar 2024 21:53:23 GMT
CMD ["/bin/sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_VERSION=25.0.5
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Mar 2024 21:53:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
CMD ["sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Mar 2024 21:53:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 Mar 2024 21:53:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
CMD []
# Tue, 19 Mar 2024 21:53:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Mar 2024 21:53:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7679290b41e2c048913474cf0c2e5caeec6ad666e9e0c95a5bc085f1e72d41`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 7.9 MB (7869178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed5af691a7bab21d5f072ee2359c6f5f3845dfaab1820f84ebf5627349c634`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e00f7927455cb1e16403bfbd1f1ba6012145c6ad1951b673f7df9c7fc001d5`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 16.9 MB (16902830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04afe6918934a3143d63818f73f2938c7a0e9ff9d1092103fc5d28e6425382ba`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 18.4 MB (18404714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728a4abb38a87c59f46cca8005cf22c072ada1076ce10c76718359c666702856`  
		Last Modified: Mon, 22 Jul 2024 23:03:25 GMT  
		Size: 18.8 MB (18816965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc39c5a0e612118a688cce82addbc8dd2ef956f7a3534d939ee237eb0ac70ae1`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a90873a8c93cb7ee93115481a37fc5fe72f772ec7069539c41c8de58d5f74aa`  
		Last Modified: Mon, 22 Jul 2024 23:03:25 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b490c6db84f5f31a63ec6e2dd6342a7c1f9c633e7681858278c783153316dd7f`  
		Last Modified: Mon, 22 Jul 2024 23:03:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460ceb608bead2d020bb56789793870b0bd6785d8d679a33d8de34f6d9eb021d`  
		Last Modified: Tue, 23 Jul 2024 00:06:53 GMT  
		Size: 6.7 MB (6655130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f357b5b0c827ea25711b2192284ca322f29f99a84c3cf8d28b8260e288775`  
		Last Modified: Tue, 23 Jul 2024 00:06:53 GMT  
		Size: 89.2 KB (89208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab47b2d81ee0fdb8595a992ba9b5d5f926f64b417ded70e53d77f951715068`  
		Last Modified: Tue, 23 Jul 2024 00:06:52 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a507254e270243d2787668bb563b86cb6525c62b7b12da5baffc3581f5b2d0`  
		Last Modified: Tue, 23 Jul 2024 00:06:54 GMT  
		Size: 55.7 MB (55662461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d84a0a97f0f6c52a213ce31287761d68d5c32235e906d081b36ddaf8d8e0aa1`  
		Last Modified: Tue, 23 Jul 2024 00:06:53 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccce10d41e11f2f294d6d519dcd2c802c854dda3a2413e0d3c79c0d2e02e9ba0`  
		Last Modified: Tue, 23 Jul 2024 00:06:54 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9457e6feeae99b1b9a418b9884fcfe68156c1cf89fc788c8ce9cc9f59bd5f6c`  
		Last Modified: Tue, 23 Jul 2024 00:58:49 GMT  
		Size: 981.0 KB (980988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c21aba154329e0ad83280ebd18063fb1ba424229a775d38b76f8707d6cba1`  
		Last Modified: Tue, 23 Jul 2024 00:58:49 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f769451673472bb0f927fb2ba162d252ac7805e0df528f22ebfd5022222455b2`  
		Last Modified: Tue, 23 Jul 2024 00:58:49 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a21ff20ace2b021ce230318aac1107812d7f3170e655f65d03b18bca5868bf`  
		Last Modified: Tue, 23 Jul 2024 00:58:49 GMT  
		Size: 21.0 MB (20985918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e8000a558d7925a01532e970f9c92b3ec806c9a9a61bdf9b1b5e7321212f9c`  
		Last Modified: Tue, 23 Jul 2024 00:58:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2cde7ea093bc573b59291d84b1297003b4922f264eb7ca7ce21fd7f9eebae289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7afa9d4431f28f5af95a44b6a818353b07283c63fd8a978a7660eefd553e1c5`

```dockerfile
```

-	Layers:
	-	`sha256:fa34cb595e9868bfd6af593b9d7994f5344ecfe38c1cfe80d10a45ad141f4762`  
		Last Modified: Tue, 23 Jul 2024 00:58:48 GMT  
		Size: 30.3 KB (30268 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:aefd2fa332c3beb1ad0644cdcc40127d0885026e7c21eafdf731285ac5860303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147113098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a136b7281e384d90ef7f716d771409e79fc73485a5a3a0ff73a57ce78e820252`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 19 Mar 2024 21:53:23 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Tue, 19 Mar 2024 21:53:23 GMT
CMD ["/bin/sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_VERSION=25.0.5
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Mar 2024 21:53:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
CMD ["sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Mar 2024 21:53:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 Mar 2024 21:53:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
CMD []
# Tue, 19 Mar 2024 21:53:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Mar 2024 21:53:23 GMT
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
	-	`sha256:77aa954d01d4a4200558075be6d053fce462a253952e1685d4adfde7ad784797`  
		Last Modified: Fri, 19 Jul 2024 18:00:38 GMT  
		Size: 15.9 MB (15907335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fabba696f4d801a629b1502ff7a225408c99800f3f45ab06a2b45c758c0857b`  
		Last Modified: Fri, 19 Jul 2024 18:00:38 GMT  
		Size: 16.8 MB (16772738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5b5f96439c536ecc4b31b76b3711886d0b4f985c3ccae78b0d5b504da52d6b`  
		Last Modified: Fri, 19 Jul 2024 18:00:38 GMT  
		Size: 17.2 MB (17176045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097cea40893c99d5cc1ccd769b7755c0995ed09b54ad7de11ea363a3fee55f2b`  
		Last Modified: Fri, 19 Jul 2024 18:00:38 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddc5449112def0b98413731c7b835bba8cf9b60341abca8646f4e23d6aacd2e`  
		Last Modified: Fri, 19 Jul 2024 18:00:39 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfabbe6fdaa90af5cb1bf7b303356df282569aec9de5f4c163600ae3e7fd118`  
		Last Modified: Fri, 19 Jul 2024 18:00:39 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa8e4b3f5cf367a1e28436492862550d4e55449077993853c3b6fd5bc881542`  
		Last Modified: Sat, 20 Jul 2024 00:50:18 GMT  
		Size: 9.9 MB (9853103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32257c434202797b41c1f752b6800cb5b96bfc4cdfe5a05e0fef2427f9bc6560`  
		Last Modified: Sat, 20 Jul 2024 00:50:17 GMT  
		Size: 98.7 KB (98702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999067dd37a285cae6b235a6e00185c24d2c9fc0ec4f31d735eb145b47419c2b`  
		Last Modified: Sat, 20 Jul 2024 00:50:18 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f426f7b65c94b7794d7d228f057b574e5cb0f69dc0871f388726a362a7aed9`  
		Last Modified: Sat, 20 Jul 2024 00:50:19 GMT  
		Size: 51.4 MB (51370504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71871abfb478dd5a0694079cd7954cf044579383c47695f98d0d9cccc1b227bc`  
		Last Modified: Sat, 20 Jul 2024 00:50:18 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be19360f94341d0c6cd75ccc4a12d09d263166267979c29d804149c5de34d572`  
		Last Modified: Sat, 20 Jul 2024 00:50:19 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d879e181b0907a1c65c74c13ec338de6c073a1ed9da0a4dd18c11ea78b90f3`  
		Last Modified: Sat, 20 Jul 2024 01:56:31 GMT  
		Size: 1.0 MB (1023176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff805453923760deeb9f62b4a08b0f009fef080462f6b2097ca404c0d64f7fa`  
		Last Modified: Sat, 20 Jul 2024 01:56:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ab8178b82a79ff32eac61c0196c646196e87425cf49f1e7bc199b614cc8925`  
		Last Modified: Sat, 20 Jul 2024 01:56:31 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c641e2f081cb980cdd3536a79135ed7b0efaf3e345de2c26e0a4df005fd9351b`  
		Last Modified: Sat, 20 Jul 2024 01:56:32 GMT  
		Size: 22.8 MB (22838652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2028f18022f1aaac7856567a34f90bac8d84125ff3363cff45d1f943739912a9`  
		Last Modified: Sat, 20 Jul 2024 01:56:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b2943063b87629fc98892f3ff2ff36c90f2477748038473ff882e2186b58d3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca9c75e9b5786ef3344997fba66a6273a64eea683d543ef94a5a151e6ce172c`

```dockerfile
```

-	Layers:
	-	`sha256:f11c69b31f5881b608429172969e09d8631db4b698dd70d5ba85d0f729dca3b3`  
		Last Modified: Sat, 20 Jul 2024 01:56:31 GMT  
		Size: 30.7 KB (30682 bytes)  
		MIME: application/vnd.in-toto+json

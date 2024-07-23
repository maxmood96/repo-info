## `docker:24-git`

```console
$ docker pull docker@sha256:f8b2a368702a25ce4cbc10c8814fa59cc80fc548ef5c6181ea56ed58422eede7
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
$ docker pull docker@sha256:b04e7166a785e25d037c712c1f2fe6912923164a21e3c369128c0cd0be92df56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126617213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f067437c5a5decaab67bfe9db6435ca9da849b70d380e730dc3c4ddce0e8f0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["/bin/sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Jun 2024 00:17:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Jun 2024 00:17:01 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD []
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

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:eeb053b6de18d715d90d4fd88a1e56001e01b8acb926c4d9040813cc1efb6c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b19c6203d20aa0e4ec2c93e6c433754dab5520e9e94b3934682a4ed1c38af1`

```dockerfile
```

-	Layers:
	-	`sha256:14c60d1db2fd1239caebe64b73a30fc80c222fb47354b846ec6349575d687e34`  
		Last Modified: Tue, 23 Jul 2024 00:06:51 GMT  
		Size: 34.8 KB (34829 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:c985f3fa651a00f95d4894b3f177e3f8535d84ed4544d2262ca975f1e66e3532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119573832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29bf4eac729e1dd2d5ed3b0eb0eff7fe310bd65f89b16e8a00107a601149506`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["/bin/sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Jun 2024 00:17:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Jun 2024 00:17:01 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD []
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acceb8f7b1778b053c01711ea320058d1fa30ea253a82a8f9e4279439f2671e5`  
		Last Modified: Tue, 23 Jul 2024 02:46:51 GMT  
		Size: 7.8 MB (7799501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ceaa340dd91ca232b4309a1884ef59234cf953c0edc16a6f59c76eb6b27ab8`  
		Last Modified: Tue, 23 Jul 2024 02:46:51 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cce1aead528994f156bb975b8de1b8fcfb16367bebd949f1e74da78e8b28839`  
		Last Modified: Tue, 23 Jul 2024 02:48:23 GMT  
		Size: 15.1 MB (15132927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df3e21cb8bccdd0ebf63ba0b2c0f9333fb1fab06b680c975bc6bd6066edae9b`  
		Last Modified: Tue, 23 Jul 2024 02:48:23 GMT  
		Size: 17.1 MB (17117277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70136a95ea7d8cdc996b7f8e32e404e68d9bcf76e84c3e28321b0c19e0cf99ca`  
		Last Modified: Tue, 23 Jul 2024 02:48:23 GMT  
		Size: 17.8 MB (17773473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ba4d3b72594e997c3f9ec312158dc583cf9a70fd84756091e1eac19516ebf3`  
		Last Modified: Tue, 23 Jul 2024 02:48:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a60703fe14dc4a8c07850201a0e94121cef00d7d0dff6844f17ff0fdc6cbed`  
		Last Modified: Tue, 23 Jul 2024 02:48:23 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074fbfb09161f618b1a22b3310e5deb0b44a39ebaa03e19364ef34780f764ed5`  
		Last Modified: Tue, 23 Jul 2024 02:48:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4573b2d4f35f3382dff2eee07e013632f516e6eddda98ef7710f71844ee1e7e6`  
		Last Modified: Tue, 23 Jul 2024 12:13:47 GMT  
		Size: 7.0 MB (6983691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d91c7fc9e4d909031ac0528fdcfd5f904450ad90e362cccb5cded48e162cf2`  
		Last Modified: Tue, 23 Jul 2024 12:13:46 GMT  
		Size: 88.4 KB (88416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6d81a29bfa206f95bae52afe2f5c82a0aae025ee19ebaea1e7d96e03524ee6`  
		Last Modified: Tue, 23 Jul 2024 12:13:46 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4792f07b753fa71e4b56378a0bd36d584057a4c597cdf90598717a9adf841d4`  
		Last Modified: Tue, 23 Jul 2024 12:13:48 GMT  
		Size: 51.3 MB (51305412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911459a771eb38ae63be8660e963661d69216a2151c3576e94852f068da22ca2`  
		Last Modified: Tue, 23 Jul 2024 12:13:47 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d805b5d770a2aea88b423b01c3583af155d0f627a7d568b99541ff5398fee7`  
		Last Modified: Tue, 23 Jul 2024 12:13:47 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:8e1a9f423efae41a57f0fbdeae92cfbcca3454aaecf0d962795d668c46f91112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b7a11f78042e9e1d3d980117eed13b43827490833fd2e6eccebc472b087aec`

```dockerfile
```

-	Layers:
	-	`sha256:a84badcd3b03e6ec65fb5fe71a6ac8572e0f205ee14c4063a9ef0fab9eb51d3a`  
		Last Modified: Tue, 23 Jul 2024 12:13:46 GMT  
		Size: 35.1 KB (35056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:aa24ac7774db1e0558aa7df804d23c627fbd87c80abf851018b75a222bda1b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119854157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e629f0763b4eb1227a88333c20921b22ed403b7300cbe49c5a9a2766467ffb95`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["/bin/sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Jun 2024 00:17:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Jun 2024 00:17:01 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD []
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc207b615c319e49e5cbb3365ee5764b9a8eea7414f19c09034fca953245451`  
		Last Modified: Fri, 19 Jul 2024 18:00:02 GMT  
		Size: 7.1 MB (7138108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c064dd1c63b0d94f8fb972f6a1d856c399d05ab32c4451f822ce452a52c0314e`  
		Last Modified: Fri, 19 Jul 2024 18:00:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcf43ea8ecd36d338b54a2cf28fe43ef2c90c169f5675fd3cc0170161cb5fca`  
		Last Modified: Fri, 19 Jul 2024 18:01:39 GMT  
		Size: 15.1 MB (15129210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574248de97671408333b7976f604cabb6878b5ed4b9bc2eaf2fbea3e95e09103`  
		Last Modified: Fri, 19 Jul 2024 18:01:39 GMT  
		Size: 17.1 MB (17104849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d27e0344e93b11956bd02b5fc9e35f4b4db1d86a540d53dcd2784567d3f2697`  
		Last Modified: Fri, 19 Jul 2024 18:01:39 GMT  
		Size: 17.8 MB (17761054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6cae0672d5e476ce351ce0de0559a2d786e8fa799af200d1326b41e76025d5`  
		Last Modified: Fri, 19 Jul 2024 18:01:38 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdeba5e488f30b2301e0f7cb3675c98b680a7019c454e5b1e245098fd2ecefd`  
		Last Modified: Fri, 19 Jul 2024 18:01:39 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a13d4ca14d7e369478f840bde21d70cf0be981c22a9b17feeb0e8dc22b1df4`  
		Last Modified: Fri, 19 Jul 2024 18:01:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc418e8349f25d7944a80019085158ce1b4a03c236c05ece474fc6f6a3efb0`  
		Last Modified: Sat, 20 Jul 2024 02:58:37 GMT  
		Size: 8.2 MB (8228158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729faaee158775d72c9a85e01f2f73c095601a9b54b882bf53e4fd59ae624943`  
		Last Modified: Sat, 20 Jul 2024 02:58:36 GMT  
		Size: 84.5 KB (84542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129304030c61624c8832ce82448639492770d573911aaf328954d588aef95eae`  
		Last Modified: Sat, 20 Jul 2024 02:58:36 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14e16bbb31b6fe1d97d9cf93a37f9b77868417f213c26f5551d84d6e374eaca`  
		Last Modified: Sat, 20 Jul 2024 02:58:38 GMT  
		Size: 51.3 MB (51305427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e077b7a06bd1837907150cee45546e6efce101d3a3b730f5beb1176d88bbce0d`  
		Last Modified: Sat, 20 Jul 2024 02:58:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93cc721505823023911ae9223323e8a2083df59cb79e2d10db30e51cafb47a`  
		Last Modified: Sat, 20 Jul 2024 02:58:37 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:e25ef189b8b9c9877757a296e35e03a8575e605a2d44afac0eff26c7eaa8d978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfa6f97deae08d47eb6e80e869bbdf7dbee4f8ba7e9292f15ed790c4909b972`

```dockerfile
```

-	Layers:
	-	`sha256:6d4f6daebf7cb708e2e2da47e9380f4afa57be8d4898e129fc1b7dcf0306abb9`  
		Last Modified: Sat, 20 Jul 2024 02:58:35 GMT  
		Size: 35.1 KB (35056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2a759b8425dba01d38f201b36885721ce41dd6ca77232ceadeed238c9386d278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121507396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b5f1408b2f4be6079741b38fc0d4ba58ce98066b9d5a774a575260dc6379ef`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["/bin/sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Jun 2024 00:17:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Jun 2024 00:17:01 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Jun 2024 00:17:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
CMD []
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

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:261ac86c79912b082bb76953790c0227ae2acf006eb017c30aab9241623d9197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 KB (35341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab296625ebefe40c7b7073b5af5b0e99caf7b2aa8e4345fae5a6819f931953a`

```dockerfile
```

-	Layers:
	-	`sha256:8eaa23e062f2ca8fb3eaf3e8c45a44fe44b64e15a922a3097fe301f166c1b41e`  
		Last Modified: Sat, 20 Jul 2024 00:50:46 GMT  
		Size: 35.3 KB (35341 bytes)  
		MIME: application/vnd.in-toto+json

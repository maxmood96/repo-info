## `docker:dind-rootless`

```console
$ docker pull docker@sha256:b3965b2e50f7d5fda2a9455c900070ca4da0cfeced964c0b432eb501b6e2e3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:88dff40d1f721a78610fe9663af845bb64927d637aefe5226b3a69f55a108397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152282040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4904946c9c358efe464ea7f4a9c756c61879cad43279619c8880e92cc7d358c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 17:04:48 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 17:04:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 17:04:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
ENV DOCKER_VERSION=27.1.0
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 Jul 2024 17:04:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 17:04:48 GMT
CMD ["sh"]
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
VOLUME [/var/lib/docker]
# Mon, 22 Jul 2024 17:04:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 22 Jul 2024 17:04:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 22 Jul 2024 17:04:48 GMT
CMD []
# Mon, 22 Jul 2024 17:04:48 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 22 Jul 2024 17:04:48 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 22 Jul 2024 17:04:48 GMT
USER rootless
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73614942b522b57819e42b44dabc585e07026466cf010fb0f8b294e3c29cdec`  
		Last Modified: Mon, 22 Jul 2024 23:03:17 GMT  
		Size: 7.9 MB (7869153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1135a6244bb6b5773eef45d5ef57a89c75b9f4fe8d090e1e2ffcce8526f42ef5`  
		Last Modified: Mon, 22 Jul 2024 23:03:17 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93dec418be19854326cc7a1500b90369878fbf97f8c4943d30ae1810b128e0b`  
		Last Modified: Mon, 22 Jul 2024 23:03:17 GMT  
		Size: 18.1 MB (18086571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd3a1e0b5ded7bbeace990a2f6219abadc88006954f65e01063519b757c7a7e`  
		Last Modified: Mon, 22 Jul 2024 23:03:18 GMT  
		Size: 18.4 MB (18404712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74253a427d4a1387474dc1da9031753eaa03f651fc77fd6bc96fed91ca29404c`  
		Last Modified: Mon, 22 Jul 2024 23:03:18 GMT  
		Size: 18.8 MB (18816952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9a1914b045cf31c2d6c0e6cbd9a3a78804012518b2e5d5eb853dccc684cd8f`  
		Last Modified: Mon, 22 Jul 2024 23:03:18 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cd54134623a2a26a4c81b0efcca08c8b78f1f5d98e97a72f1e9989f8cd1f29`  
		Last Modified: Mon, 22 Jul 2024 23:03:18 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89841116322b5231e9fb3ab3752b5742b48207f6abc09621d5b87961afa0b87`  
		Last Modified: Mon, 22 Jul 2024 23:03:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569c73127d339355bb4ad68cca52beafe2d36c88ecdb00f0bb30e960f173ef45`  
		Last Modified: Tue, 23 Jul 2024 00:06:49 GMT  
		Size: 6.7 MB (6655113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1921992dfe475517dd86f9019bc75d5ae3dfb4fb3bbb7d40d1e8a8ac12f0706d`  
		Last Modified: Tue, 23 Jul 2024 00:06:49 GMT  
		Size: 89.2 KB (89204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a1d54016c3ffb08c6da2f8ed0ee1fbf097ac90542379d556323432ec4903ef`  
		Last Modified: Tue, 23 Jul 2024 00:06:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9565c510616fe97ca636bf5c0b2fd7443423c8fe7155344fd822d6b0460cabcf`  
		Last Modified: Tue, 23 Jul 2024 00:06:50 GMT  
		Size: 56.8 MB (56767404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c441fb89f312ca7e033e498bbfd6f05217891ca24d28e0c3f8fcc0943a2161ff`  
		Last Modified: Tue, 23 Jul 2024 00:06:50 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26ac0d476d8731ac10ca8457c54795f86014cc766ef61710276c0667e350e5b`  
		Last Modified: Tue, 23 Jul 2024 00:06:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b4ed69d59d4cc1d963367141be4dc24cf2f3d221a480590c50f27f7d693c92`  
		Last Modified: Tue, 23 Jul 2024 00:58:54 GMT  
		Size: 981.0 KB (981007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6463b65df3d7dd154742665fa23be57025c4ed01c5cb9506bba4e7428eea8195`  
		Last Modified: Tue, 23 Jul 2024 00:58:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46b13a006cc7a5446496288d22d106bf628f893002e8a95ae19ce61f0b94c`  
		Last Modified: Tue, 23 Jul 2024 00:58:54 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8973976d6819135155e3f171b74b958f57ef45ea727957f2b39cb126f966e895`  
		Last Modified: Tue, 23 Jul 2024 00:58:55 GMT  
		Size: 21.0 MB (20979741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aeaa68fe76fad717b922483687303bbfedd080ef4bb9348a2b1e4f7e7aa487c`  
		Last Modified: Tue, 23 Jul 2024 00:58:55 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e88eff02505c9e085f2c6b1b36ddab93219d1f835b850b45de9d2e1b343d4cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af2f25d91801af23449cfc4c4d00a408e985da7cbfddcdc5cb7d39c78848ab6`

```dockerfile
```

-	Layers:
	-	`sha256:5bca1d49a4db2b903966e4faf56a5e189607af4193c8a1657eec2d4cca96feca`  
		Last Modified: Tue, 23 Jul 2024 00:58:54 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:674a57d697168b1938cd95ac1e309777533bef21adb97bcf1fb17aa80b67e780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149238220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb864fcf4e7001a6be148c952bf18519b2f66fc5a06e1911f1a989a662e96e4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.0
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-x86_64'; 			sha256='fb3f6c317056ec54e8756851663ca788521f7a9c60afb8a595bc7a05ffaa8951'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv6'; 			sha256='e1f2942bff7e16556675e46db6e30d6ecbed2e78656c760b8e25383817b7a328'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-armv7'; 			sha256='7ca096778a30c349816f67ce772709164eddaf3022901bf55472ae3134264cf6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-aarch64'; 			sha256='49941418051846d72c74dd8df1f8b4ff753ca74d29986361d937384fbfb63569'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-ppc64le'; 			sha256='45606de42e140e20eadb7f8a9db62f783de7df6c148640cd67cf8f9ef3aaab99'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-riscv64'; 			sha256='e685bb6ad60225dc099acf85cfbb928e5ceef26a1a61f4995d1fbabac438d0e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.0/docker-compose-linux-s390x'; 			sha256='94622d0476d9f59b40c24daa22231c603a93fd9acc984c4427ca946dfb4a908c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD ["sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD []
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea605edb795ede26be75c45e9007c2b3174e3b67789da721de4d4d9821301919`  
		Last Modified: Fri, 19 Jul 2024 17:59:44 GMT  
		Size: 8.0 MB (7974734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679037bd9e35b2e299f0007ada944ba7f3d610a1d23e8a9c753d82a2ca2ec165`  
		Last Modified: Fri, 19 Jul 2024 17:59:44 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e324a196ce93131dbb3ad7ee9222e0379665036564e6db56429c96bc3a8719`  
		Last Modified: Fri, 19 Jul 2024 17:59:45 GMT  
		Size: 17.0 MB (17028618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e685dd4691fe103ea0688f0644e00840ce815f6510ab8515724bdee158a3dd92`  
		Last Modified: Fri, 19 Jul 2024 17:59:45 GMT  
		Size: 16.8 MB (16772764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ca2677246d2352528cbc6572e638fc4d142301d15c3373269980a06249dc6b`  
		Last Modified: Fri, 19 Jul 2024 17:59:45 GMT  
		Size: 17.2 MB (17176043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04eb492771ef57329ce0d94a9c84cc355d40d41fe2ae2e02204b3e1cf804be1`  
		Last Modified: Fri, 19 Jul 2024 17:59:45 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027486f133acec62c5f8737955492c6f7e1d112ee2d801892ef87ba4c0dde075`  
		Last Modified: Fri, 19 Jul 2024 17:59:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2745e109244d79b17f02d10defd0ae9dbc1bbc19bf1ccb189a11a467df37baa6`  
		Last Modified: Fri, 19 Jul 2024 17:59:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2522f3cc4dd2b359111312845faec852e1cc26195177ab95057fc09f8e0157f9`  
		Last Modified: Sat, 20 Jul 2024 00:49:15 GMT  
		Size: 9.9 MB (9853071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f77eb4a9ab917a114c160b9278f46a7a4f19015545b8e6cae90892ac175b88`  
		Last Modified: Sat, 20 Jul 2024 00:49:14 GMT  
		Size: 98.7 KB (98697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134876d02e5ca7ce993beefae79697bae24524b2683b5bbece45a4964ba8e687`  
		Last Modified: Sat, 20 Jul 2024 00:49:14 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1143526db0cac620a43849dd4cf3182a4e680a2302ea2b931073f7d4e80a43fe`  
		Last Modified: Sat, 20 Jul 2024 00:49:16 GMT  
		Size: 52.4 MB (52376023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad23f2508c170fe809fc43df91ec55508adc70bacc9cb8312c47856f780eb28`  
		Last Modified: Sat, 20 Jul 2024 00:49:15 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2410909ee57bcc6e20bad83e13c11dbc21bdefb6618002257b57749c4fa7d2ef`  
		Last Modified: Sat, 20 Jul 2024 00:49:16 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9875ac98afe78e9b48028f4814c86e9bd97fa79d5b17f42683aa5d907099fe5a`  
		Last Modified: Sat, 20 Jul 2024 01:55:33 GMT  
		Size: 1.0 MB (1023188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50eaa54ba999668290dcbe2aa925d6712c0b18ebf3da5d3eda581bc36e75f86a`  
		Last Modified: Sat, 20 Jul 2024 01:55:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb41b2f8ffd411abe88ed93fe2ed9709b53406de861f78fd174c7eec76f58112`  
		Last Modified: Sat, 20 Jul 2024 01:55:33 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cfd74a9d348277d80a63182de64a70712752a80cf2aaa43522d815d120557c`  
		Last Modified: Sat, 20 Jul 2024 01:55:34 GMT  
		Size: 22.8 MB (22836978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144186fbc3f6c6262fc38100db241210ec3477e3e4a0033dc6e31cf94acbfe59`  
		Last Modified: Sat, 20 Jul 2024 01:55:34 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:452c03e9886c8d6d672d49d667b62c0988601290184a2ecb2f7300d945a21d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07595bc529eecd34ea075276beb1f0cf9cfe001f3962d0661ab7ca7b203f86be`

```dockerfile
```

-	Layers:
	-	`sha256:328fce7256ac888b801262d64047556e2746aabbe0ed240632d5fc42df03ba12`  
		Last Modified: Sat, 20 Jul 2024 01:55:32 GMT  
		Size: 31.0 KB (31004 bytes)  
		MIME: application/vnd.in-toto+json

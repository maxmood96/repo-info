## `docker:24-git`

```console
$ docker pull docker@sha256:8c03e50da9c505a73c79a686103415deced3c935cb5f91463fb3e6227aff8ec1
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
$ docker pull docker@sha256:32cb6704300c569008ea8dab5197f5948b6d972545496c59e63ab46af9d5570e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129024395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c978a43b85cf920f2b3df6d8e36f92b77ed2636e9a52bc257fa0b933892b7a6f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c6e97cab05fd4c36d1feb09dd1df2562790b1fcb30e99ee9abbe4d82a502b4`  
		Last Modified: Fri, 19 Jul 2024 17:58:21 GMT  
		Size: 7.9 MB (7869255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6270b9922ccd2919b2a34b53a202d98063fa64dc14a33879bf0bdcc27519a594`  
		Last Modified: Fri, 19 Jul 2024 17:58:21 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b8481a37d57ef9411c9581960789b353eb8cea52b36466f6c58d21abc7ce09`  
		Last Modified: Fri, 19 Jul 2024 17:58:21 GMT  
		Size: 16.4 MB (16410679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091322bc0ab9d84c1a6085974f9e652e677778d7cee1630d5283d26ec8db3697`  
		Last Modified: Fri, 19 Jul 2024 17:58:21 GMT  
		Size: 18.4 MB (18404716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50879ee4f517f969597d7516a254ba79d18c09ab4971e74afb89a52e3136e0e`  
		Last Modified: Fri, 19 Jul 2024 17:58:22 GMT  
		Size: 18.8 MB (18816952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d293990857f77c096f7622e4ffb8fa4cc612be0ba1ca3d10d4ab77b279389aec`  
		Last Modified: Fri, 19 Jul 2024 17:58:22 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfebfeb6175b0d2d1e7ad9a6144d6eb62416e73f7fe065b2d9b933fb4f022748`  
		Last Modified: Fri, 19 Jul 2024 17:58:22 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e827b74e56bfed9d29791b96a00c69f3f4a0453096b798363725a017edd62e`  
		Last Modified: Fri, 19 Jul 2024 17:58:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f6c2962b67bf5c871315822072223900244c51a9551636dc0c19ddac617338`  
		Last Modified: Fri, 19 Jul 2024 18:59:59 GMT  
		Size: 9.1 MB (9061188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec8b34c5fb46387ea7601bce6ed356eeff9736efad6c7c7a134ba54942a0cbc`  
		Last Modified: Fri, 19 Jul 2024 18:59:58 GMT  
		Size: 89.3 KB (89262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b16a08359aa1fcbf5dfdf588ad323456bfe5aa72501b407633a95e9fb6db54`  
		Last Modified: Fri, 19 Jul 2024 18:59:58 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f815bf025fb90081670beb795189b667794ca69b9d848c6e22d702cfc191aae5`  
		Last Modified: Fri, 19 Jul 2024 19:00:00 GMT  
		Size: 54.7 MB (54740554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2917934e3467dd6268b633bbdfe34c60b560e7597e2f6b1418d9257fedfa9660`  
		Last Modified: Fri, 19 Jul 2024 18:59:59 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aa4aa0b3a449b55d4c453a019d9c041eb575642ef8c2af66dc0a0c369bead8`  
		Last Modified: Fri, 19 Jul 2024 18:59:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:bf8e1467eabbf7fdaa37600e1451e2e86ef773418195150802dd119931281b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7dc9fe3c2b531f152d3d93cb7a28665f72b4e0569c0057150d1e2b96a75e34`

```dockerfile
```

-	Layers:
	-	`sha256:9d5b42ceb841d3b8b756b00ee70b73cde8be1993910381d77fc54c25545efc77`  
		Last Modified: Fri, 19 Jul 2024 18:59:58 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:fdd47234c0634d19a8e2f768878d899cb702871734f4bf1285bdbb4c0d77e26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121648901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe5f2f1fc32e0e3b12ac934d7bea5cc23af16677efff0a785c03896f7a44557`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f37c167e489c1fd415ada79fd4d6662e15882e8c1db0dcd3bdd378f575ec2bd`  
		Last Modified: Fri, 19 Jul 2024 17:58:15 GMT  
		Size: 7.8 MB (7799567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb9171d6acb833cf25c1d208a00566eec38f1d27110fbc6737de85a1382356`  
		Last Modified: Fri, 19 Jul 2024 17:58:14 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945186ccd9875b1456adb1a9af589c898779ed0b6daaa101dedc739d8daef28c`  
		Last Modified: Fri, 19 Jul 2024 18:00:05 GMT  
		Size: 15.1 MB (15132930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532ea299dceffbcc7b4a77c05edee9bf13a654ce2b6876c423871bcd8dc37afe`  
		Last Modified: Fri, 19 Jul 2024 18:00:05 GMT  
		Size: 17.1 MB (17117268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b51781a3c2d77f56050ae7bbffb8baba49c6a338e7e0439f41c0641efee91b9`  
		Last Modified: Fri, 19 Jul 2024 18:00:05 GMT  
		Size: 17.8 MB (17773466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473cc5dff51346a8aec505111405fea4852accf8d9a12362843f6a86be5738b7`  
		Last Modified: Fri, 19 Jul 2024 18:00:04 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd4004cfa4f946dc1ffec7a34e763908b6cde10599ed7de4e12966c22462feb`  
		Last Modified: Fri, 19 Jul 2024 18:00:06 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc0c0c972235351d7435304ba3bbcd1e10833948c3662e8a4b40991077876f8`  
		Last Modified: Fri, 19 Jul 2024 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc9958bbda82d3822b6a52db9da8eb02ad083fd971046f76d3cff6042b7a7c6`  
		Last Modified: Sat, 20 Jul 2024 00:12:18 GMT  
		Size: 9.1 MB (9056709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359f1868d97a691c7599b7c7c54b6a4585e060159e213c982d63daceb95c3503`  
		Last Modified: Sat, 20 Jul 2024 00:12:17 GMT  
		Size: 88.5 KB (88457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0444de25f5b2d49fbd30cef87bf2dd9db33e2da3954c809319ab96a75540ad0d`  
		Last Modified: Sat, 20 Jul 2024 00:12:17 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc639a149bc4b924e9685681ab8fdb41970c350ade5a7e5b980c5cb3481a19a2`  
		Last Modified: Sat, 20 Jul 2024 00:12:19 GMT  
		Size: 51.3 MB (51305410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06890157d28b531973034bc233eb15a028b9fafd62a735fba086aa0626739fde`  
		Last Modified: Sat, 20 Jul 2024 00:12:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b646ba44ffe1973721184176e771099d420fefe4fba92060cab8a19e9aad4f`  
		Last Modified: Sat, 20 Jul 2024 00:12:18 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:df179f44ef9ae857e8c53091eb6c20a481f74fa7d9fa557db1f2240c7f774d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48846078ccc0ad503b7258a440413f803c38ce817b6a27f845936a03b58d3dd`

```dockerfile
```

-	Layers:
	-	`sha256:cdc26d05c91c695510e6bd541e337aedb0af757e69feba649d7a0110c1b36d70`  
		Last Modified: Sat, 20 Jul 2024 00:12:17 GMT  
		Size: 35.1 KB (35055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:58957d800df9f018ce38d821879088bd37164876293a470d60602bb2b3898266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119853737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548fbc483fa4aee228a772c31b3ad0406720b7a1250f021e70d8ee3058c49b62`
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
ENV DOCKER_BUILDX_VERSION=0.16.0
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-amd64'; 			sha256='9a9a6ca0b929a57db01020fb226b1a2ea2bc57eba63d4adec46c43d0009506e2'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v6'; 			sha256='902f1240a6071c721f9746f0ff0859ef7b7368b683e322c08a1daa92d61d698a'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm-v7'; 			sha256='81d53f05d1d02306844f5a364cae6d7ad24451497c171ee29e1c000a78f30c5c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-arm64'; 			sha256='1aa8f0438866c706654a6dd96e211e509d42b16b1a0e66c1777c95edb2f14f49'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-ppc64le'; 			sha256='569f4a47bca797385eccac18e14e1d4bb681e35eeff6304c432de5bcd543120d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-riscv64'; 			sha256='e0cfc5072a792088115560e77a8540c9bf8299716984d42adc0735161472f076'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.0/buildx-v0.16.0.linux-s390x'; 			sha256='80ff8dcddbc3d0306e5cb819eddf89ce970ea1dbf806eb0adf7b6cd616d1da63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
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
	-	`sha256:16f9c1cb3f348935ccc2213b45a6f967fb9ef04e90990caa00fa3a8df1888bc1`  
		Last Modified: Thu, 18 Jul 2024 18:55:14 GMT  
		Size: 7.1 MB (7138017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179c5d549bc55c8b6f2281001fff6db882e560d7da01693827da1c931a9a8692`  
		Last Modified: Thu, 18 Jul 2024 18:55:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4696e0a3cb38053797fe70e578f444c4e9371828d68b0b848b25cc706dc261`  
		Last Modified: Thu, 18 Jul 2024 18:56:44 GMT  
		Size: 15.1 MB (15129215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12958a02f0b4adee017b8fae2d0748360fe339e585aaee189998d54278529fe7`  
		Last Modified: Thu, 18 Jul 2024 18:56:44 GMT  
		Size: 17.1 MB (17104578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bac4196212ee5f8fb710f6051d93d809bcc7337f349687301cdf88ceec88a0`  
		Last Modified: Thu, 18 Jul 2024 18:56:44 GMT  
		Size: 17.8 MB (17761047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d50c32fd04c72f9291dbd370b0f7ef201af637e3de787b7c81e4a575e542050`  
		Last Modified: Thu, 18 Jul 2024 18:56:43 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804628fc8fc1b264f841cf1c5710e60657e3fcea02d2e1c78d1471ca45beeafa`  
		Last Modified: Thu, 18 Jul 2024 18:56:44 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14606c2804bd3b5fd1056204642ef66e60f1a5273a616674aa2fe6bf6f6c1872`  
		Last Modified: Thu, 18 Jul 2024 18:56:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3addcac49bd85a818399edea94b41f945d81c2c88b6fce13356b10574d03f227`  
		Last Modified: Thu, 18 Jul 2024 19:52:23 GMT  
		Size: 8.2 MB (8228097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f160f0dbe7cc04a83fe5824957c772074f93d11c99afb662d6001e08d75b0204`  
		Last Modified: Thu, 18 Jul 2024 19:52:22 GMT  
		Size: 84.5 KB (84540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c09f2fa2da1b675272ecd4b336c96795623206beb198a36381e62bd00ef157c`  
		Last Modified: Thu, 18 Jul 2024 19:52:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b937fef021e8fb8e745d074e95e5b95cdfaa7cab85739ca8e2132ad231219744`  
		Last Modified: Thu, 18 Jul 2024 19:52:24 GMT  
		Size: 51.3 MB (51305437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ab2d1396918d0704ca07028b9ca0d61a0c27bf95c8a1769909a8db9927c101`  
		Last Modified: Thu, 18 Jul 2024 19:52:23 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e037de90a15eefc133a673c3a1a1fa311534f3b05a0b149480825ca8c15bc97`  
		Last Modified: Thu, 18 Jul 2024 19:52:23 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:b73960bd22fd13adc09c56d60d4ba3a23e691f7a8da1218245fc6c5933a7a2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b07a213c1407dfc53742c388b9153cf98fd68732918d1c25840914ee11ee5e`

```dockerfile
```

-	Layers:
	-	`sha256:8a7a28c3beaacc943054076435048a18a0499d52c190508438c2ee4672583f65`  
		Last Modified: Thu, 18 Jul 2024 19:52:21 GMT  
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

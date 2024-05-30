## `docker:25-dind-rootless`

```console
$ docker pull docker@sha256:9272705cf26c39f38a367e24ac29ad8ddf3cbfaccf86ddfe156a6d428f751ed4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:25-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6e958c59a5b4b0a2d529ae1c182c721d6f9f9610038744c23a6dfd4b57f5b6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149637585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c854419dca542c247d011baedd17b71d1404e387f4087807f84a85820471b8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 19 Mar 2024 21:53:23 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Tue, 19 Mar 2024 21:53:23 GMT
CMD ["/bin/sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_VERSION=25.0.5
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef85131bd2d2dd19cf6d59203adb8be938ddad261a59e72927548903a07773fa`  
		Last Modified: Wed, 29 May 2024 21:59:13 GMT  
		Size: 2.0 MB (2010475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196a66cdad55ee5d6dd10d536085ab782031b06766621fab9c481c0a5a75d726`  
		Last Modified: Wed, 29 May 2024 21:59:13 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8290a1efd6863a54ed0bae2c16b840f92cdee75de496a36c3a204039744a0`  
		Last Modified: Wed, 29 May 2024 21:59:13 GMT  
		Size: 16.9 MB (16902849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e81327d8175dd4e7059f8866a96c112c34c3c3871c19a4dc4a280d698be75f2`  
		Last Modified: Wed, 29 May 2024 21:59:13 GMT  
		Size: 18.1 MB (18089093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a57735501d9bb3386d3915ad44d95732276688a548c36d79ce2755e89697de9`  
		Last Modified: Wed, 29 May 2024 21:59:14 GMT  
		Size: 18.8 MB (18776601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0353e9a95649374197a19b91d685db07511daf8dcd6283ef0048112292034b3b`  
		Last Modified: Wed, 29 May 2024 21:59:14 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62e5568d130767721d648e503b2a4843d807dfbffbc259bfa708fe1e875ebcf`  
		Last Modified: Wed, 29 May 2024 21:59:14 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab51f1f93dae693b86f697557452e95b6f7bee812494c6f9f6f32472b75f30a9`  
		Last Modified: Wed, 29 May 2024 21:59:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88460bbe7e5c476782dfaf4b8b8665053ca3daaf7091db20c1665d4faeb92b8e`  
		Last Modified: Wed, 29 May 2024 23:00:58 GMT  
		Size: 12.5 MB (12508647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541427012b3f314aa3d38fb8be662d5286c3df53e35809478980c25d8f8a65f5`  
		Last Modified: Wed, 29 May 2024 23:00:58 GMT  
		Size: 89.2 KB (89183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbf44694687a5847e5b16f05961c429bdc01f66a3fd7af546106a675a917b7a`  
		Last Modified: Wed, 29 May 2024 23:00:58 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d819ef2491970bc4101a2ade5e0b2dfbeda36edac06ae5fdb9e5a8317b7140d`  
		Last Modified: Wed, 29 May 2024 23:01:00 GMT  
		Size: 55.7 MB (55662456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7673100ecbd932be7512c6000892146eef6348db858f175eaac264566b669997`  
		Last Modified: Wed, 29 May 2024 23:00:59 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939b35630fb8816234d07ec9b576c74d5f9c31105795152c512ad886ff5fe662`  
		Last Modified: Wed, 29 May 2024 23:00:59 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798498c36e6c87234b45c891415ece0035b561668b6564695ac07e94160da258`  
		Last Modified: Wed, 29 May 2024 23:56:54 GMT  
		Size: 981.0 KB (980957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efd93ca58d802dd8cfd4bea3c59c95d7546586b52a538b719198dc880d73fd2`  
		Last Modified: Wed, 29 May 2024 23:56:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16f594511a1f7e622dc37fc12cba6c46f65d373120cff98f0df7ae12a7afea0`  
		Last Modified: Wed, 29 May 2024 23:56:54 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44753181879ec5e8138a43fe512b266e05a830ba7d04977626ad698c77b3dbf1`  
		Last Modified: Wed, 29 May 2024 23:56:54 GMT  
		Size: 21.0 MB (20985921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d880ce1117967d054a74940c851e72dc75f7fe4e8b5597244fc8cfa07b43bf`  
		Last Modified: Wed, 29 May 2024 23:56:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bff401931434eff74e714f47d19466ce930c4018f0dc869930f4257cbf5bfd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a26bea033af826d2e76bb59b12fdc10b1368245cf011c62c676d77253da4b2`

```dockerfile
```

-	Layers:
	-	`sha256:2973bc4925c541d2c08a51e5481d5f26bba624120409e805082e65003aee521b`  
		Last Modified: Wed, 29 May 2024 23:56:53 GMT  
		Size: 30.2 KB (30225 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:243de9985579421ac2a6b420abda9bd59ae3cd1374ed06fc67b09a32cc4dabb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143929890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208fbcad3013b21b254999b847b13d6fecfd4853bb6eb46d55d9184273939e40`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 19 Mar 2024 21:53:23 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Tue, 19 Mar 2024 21:53:23 GMT
CMD ["/bin/sh"]
# Tue, 19 Mar 2024 21:53:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_VERSION=25.0.5
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-amd64'; 			sha256='68e4f8895331ade982de8085a8c137b8af65f3ef95040b6c6113552243638508'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v6'; 			sha256='afa9324a987d71891a8a55d33fa913e4464377c71e7cc84ba68a5d4c5e803f74'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm-v7'; 			sha256='32f0f7d30e498c1461b97b2591e5ed348e69b6d864243a838db6d2e6dc08144d'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-arm64'; 			sha256='82e776e50a84293c160e8c89c125b7a86295c7aa7f30751d6a7c051c171762c1'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-ppc64le'; 			sha256='64b62a17df3b0cd5bf88a1bc3f83cd50ebd56b403c2ebf4668b5d697fd324bc0'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-riscv64'; 			sha256='32042b4dba38724404a063ee9851ebea1c85b46ebbfb58e7350ece04975fdc9c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.linux-s390x'; 			sha256='c273b1801cdb2c78079f9c33ecec266d5104973254e4e152d0205f14d7bf7bfc'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 Mar 2024 21:53:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bff5120b86ac33e19177ec896d4d5049e656877d728c74bf1d6ad51be389ab`  
		Last Modified: Thu, 30 May 2024 05:24:10 GMT  
		Size: 2.0 MB (2006605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177edc7d05485b510d768d84b0082dd4b3e7262dd9327fadf7299fa577e0ab33`  
		Last Modified: Thu, 30 May 2024 05:24:09 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afb9c37ce4968ec987adebdddd139d14737503506b5ba2d260bb9be3b12d02`  
		Last Modified: Thu, 30 May 2024 05:35:42 GMT  
		Size: 15.9 MB (15907330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44da739efd1860fe1e38c39742448da074a1123483e659063247fa76474d6f9`  
		Last Modified: Thu, 30 May 2024 05:35:41 GMT  
		Size: 16.5 MB (16450834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175798fe1545b77478188d3570da73ca7aad276547fa4e19c7b0aafce0cc2c17`  
		Last Modified: Thu, 30 May 2024 05:35:41 GMT  
		Size: 17.1 MB (17144846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b237824f746635d157285487e5a33d3bc7531bfde5482aa81310b25683002cbf`  
		Last Modified: Thu, 30 May 2024 05:35:41 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9351c024d6902f6333fe91eb87f2034975a468d9aae56d35a17eebaec487d665`  
		Last Modified: Thu, 30 May 2024 05:35:42 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce1767f3c904a6a8a4f7e5e82f661d9ba69283911ce7e2e4661d2bd6047ecb4`  
		Last Modified: Thu, 30 May 2024 05:35:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39899f3bff60822ab77019b07b615e56522c7a5198d4fc243c617bdcc5d6bf72`  
		Last Modified: Thu, 30 May 2024 18:50:11 GMT  
		Size: 13.0 MB (12993403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66de7cd2f915a96660ccedaefcd36016a67b107f8282ff4a067d8d3172e34100`  
		Last Modified: Thu, 30 May 2024 18:50:11 GMT  
		Size: 98.6 KB (98611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4788ebe6769b6496ab7d45fc9f81466c449b22b7407415252723e6afb6643547`  
		Last Modified: Thu, 30 May 2024 18:50:10 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74cb2ccebb76a77694652925017da1d1ec2368bb9301c631af6e54be5cf302f`  
		Last Modified: Thu, 30 May 2024 18:50:12 GMT  
		Size: 51.4 MB (51370504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595455e34f6be1388e16cc5faf9ca3a66cd1793fe43f9679a07b9c3931ead907`  
		Last Modified: Thu, 30 May 2024 18:50:12 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f203f82549a22d980952392071fc3ec8212b17e83f61ca172c89c9e4b81d07d8`  
		Last Modified: Thu, 30 May 2024 18:50:13 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409de686431cf69dc525464f99177b1e201406bd0013c4654c07bf782bdcc6f3`  
		Last Modified: Thu, 30 May 2024 20:52:12 GMT  
		Size: 1.0 MB (1023060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f590c0e8ee20b7fb8028e7d793ae454651f9f5b0374f3c7bfaae63105705a549`  
		Last Modified: Thu, 30 May 2024 20:52:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4adb0d81e9b91f0c5d9b6146367a84fc5ec0fde32c0dfdbfa7e205d470c478`  
		Last Modified: Thu, 30 May 2024 20:52:11 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1533f49491624c051551d03dcedf7c2399d9d6200e4763c68283dac21f92ee2`  
		Last Modified: Thu, 30 May 2024 20:52:12 GMT  
		Size: 22.8 MB (22838616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a2e2854183e84561c010cd687a6ee476da18038c27130b4ad1e2695ad7ec5c`  
		Last Modified: Thu, 30 May 2024 20:52:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7a033b457c57319b822344e5cc2d43ad09bde2478072a0866ed091b9375c8cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff9329bd8b9e8bebe8f4a140499c65fafd1c035f8918b05121e59bcf5e868e5`

```dockerfile
```

-	Layers:
	-	`sha256:1cf79cac4e71f594b6f670e9f29a89548b039f58892617570baabddc33578d11`  
		Last Modified: Thu, 30 May 2024 20:52:11 GMT  
		Size: 30.6 KB (30639 bytes)  
		MIME: application/vnd.in-toto+json

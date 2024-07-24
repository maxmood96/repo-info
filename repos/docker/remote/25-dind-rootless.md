## `docker:25-dind-rootless`

```console
$ docker pull docker@sha256:f6619247b3dadd2b2ca8161e0b7cd376ee049785c8e8c0da42f6873c9785aeee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:25-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:686200f9cb8816b8d30af63628a5aef81c7a5d98aa3fbbc9dd275dafe2ee490b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150001536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8010a96468b52f44c37ed6bb6492a355190f21d8b51c90c46a95adf852fc759`
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
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0fb967690c83552d01047d5fb254535f8b1ecefc376c1085df22392294f3ac78`  
		Last Modified: Wed, 24 Jul 2024 01:08:38 GMT  
		Size: 7.9 MB (7869162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0351300cd3cc5ed8c0ba4263f020cb5914c55e02780c573b2f3174bc7a12395`  
		Last Modified: Wed, 24 Jul 2024 01:08:38 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74666ae82fbd8393fc9715030a10c126e757122fdaa6d556ea7189178fd02baa`  
		Last Modified: Wed, 24 Jul 2024 01:08:38 GMT  
		Size: 16.9 MB (16902828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ae1786ebb2f44a0028cf0d602453d51b7b76f188677ef492543b989dae2da2`  
		Last Modified: Wed, 24 Jul 2024 01:08:38 GMT  
		Size: 18.4 MB (18404718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08024e4da4e0cf13b89e946af0e9ac89ab750302a5d6e1c589901ee0e32f1be5`  
		Last Modified: Wed, 24 Jul 2024 01:08:39 GMT  
		Size: 18.8 MB (18818930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d4cddf888e1783363942639ae85aaf000064a5225de186a1a620fceeaf2e58`  
		Last Modified: Wed, 24 Jul 2024 01:08:39 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08616de00fb3cecaa6714a179a2f1c88867f7d44ba150bd5f383a2f2e2bc0e9`  
		Last Modified: Wed, 24 Jul 2024 01:08:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19c442b48cea1b6c18df13608d88b13d3c8bf60c8f612acee5fac57d9e0cb6f`  
		Last Modified: Wed, 24 Jul 2024 01:08:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d351a93e12b09b4e6ab120b1154051255a90ec82340385798dbb17141181de`  
		Last Modified: Wed, 24 Jul 2024 02:03:42 GMT  
		Size: 6.7 MB (6655135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd46c10bef0b3ca706e18aaa0bfc5d5ada9d3b3115117f13e2ce363d954144e6`  
		Last Modified: Wed, 24 Jul 2024 02:03:42 GMT  
		Size: 89.2 KB (89205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4a551673e81baf2169a135adfbace48c8208b472747ed436fc1a701fbf541c`  
		Last Modified: Wed, 24 Jul 2024 02:03:42 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427813a6fe1270b2786fbf785da23d599ea240d0173ff1d0471fe1ebcfaab7a`  
		Last Modified: Wed, 24 Jul 2024 02:03:43 GMT  
		Size: 55.7 MB (55662461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3c83b2992b65f453cbfb5ba8f21b845154de53e16f48ee72a7d8b127173cde`  
		Last Modified: Wed, 24 Jul 2024 02:03:43 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bd4fcd31f0dab9208f91a79112a4c8406eb4fd59897d5c6ee199cceef48dfb`  
		Last Modified: Wed, 24 Jul 2024 02:03:43 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8035e867d005155ab15c3f6770ccd2d5fd499a736e98577e71b9e63f04d7553b`  
		Last Modified: Wed, 24 Jul 2024 03:04:04 GMT  
		Size: 981.0 KB (980990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe28ed90c7a20e037a466294f572e4a33b39de1f31381b541e7e722503465a1`  
		Last Modified: Wed, 24 Jul 2024 03:04:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853f77cee29736d05c829880bd6828c5a85341c3f936b4af870fde2ca1296bd8`  
		Last Modified: Wed, 24 Jul 2024 03:04:04 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947893c41606c0cb855c8fbae8e98322fe572be7cc1e04a030687d19878a67d7`  
		Last Modified: Wed, 24 Jul 2024 03:04:05 GMT  
		Size: 21.0 MB (20985917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a273d2d0ab401c6689ea1b3c9469950e89deb2f9622288b5f68bbf148d169153`  
		Last Modified: Wed, 24 Jul 2024 03:04:05 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e568721c6b9d61b803758d7cdc1fb2ba192c7392ea3d0b43680b3c12572d0b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf50d471f71153f7a2b6a32db6f099c093b4adbf7983d472df1738dfd1683a5b`

```dockerfile
```

-	Layers:
	-	`sha256:9f7079b960eec33d34975517dde73b02189c50e4f7b61e6c7f4681863325019d`  
		Last Modified: Wed, 24 Jul 2024 03:04:04 GMT  
		Size: 30.3 KB (30268 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7f6aa726f5762b58fb57dec0ba4a7b74949e1d1ba46560e885c2f045e8c7e08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144298597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567c8b9dda07b488cd569976c9b7d401b2f950dbf982a431aecd5f8c72fe082a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 19 Mar 2024 21:53:23 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
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
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 19 Mar 2024 21:53:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92a79a211e9d2795fd6862e20d285be2e32204ecf133a96c45fc447719c6ffd`  
		Last Modified: Wed, 24 Jul 2024 11:44:26 GMT  
		Size: 8.0 MB (7974652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82180daf56b45cbe34e984171eb389836179453c540ac437fb696fda30111af6`  
		Last Modified: Wed, 24 Jul 2024 11:44:26 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d992e63d1c4ac6d8081f15a2e446186a4be5b3302933767e635cfad3402889e5`  
		Last Modified: Wed, 24 Jul 2024 11:45:17 GMT  
		Size: 15.9 MB (15907343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a866825bdada515ec43e2f8463cddee3ae0f4d7651674bccf0485a61db1eb8`  
		Last Modified: Wed, 24 Jul 2024 11:45:17 GMT  
		Size: 16.8 MB (16772739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dca544809af3e7ef9668a08de2114de7d169c077e4826a45981997b3222295`  
		Last Modified: Wed, 24 Jul 2024 11:45:17 GMT  
		Size: 17.2 MB (17182720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d093b92542b2e113ad1697526317dc8e3f7a92ab31d1846a10fd5d56156a7fe7`  
		Last Modified: Wed, 24 Jul 2024 11:45:16 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477b81460fcbe16848d3c186dd3c525f9bd838580a46005f556c7ecf74f10b4a`  
		Last Modified: Wed, 24 Jul 2024 11:45:17 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d268fe3ed5e178b1db11298201899dbe6eb436c55263f51ef0bd6c7c988e4f9`  
		Last Modified: Wed, 24 Jul 2024 11:45:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1890d568048c74a811d9fbab8bf2b8fe9d239d09cf143ea953878310c341db`  
		Last Modified: Wed, 24 Jul 2024 16:35:09 GMT  
		Size: 7.0 MB (7034000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb3ed442abacfc77f5a4a8963bdb5ce92bb69ce22dab72d748c337e051b3569`  
		Last Modified: Wed, 24 Jul 2024 16:35:08 GMT  
		Size: 98.7 KB (98655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff99b84406af3f1af420e366fba0e6c3ef87e552a919f6ca7c704450f1c3246`  
		Last Modified: Wed, 24 Jul 2024 16:35:08 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47748f1f8ea7a281d5e5361f31b0a8633c71f149d6064f712ed748ea05091b68`  
		Last Modified: Wed, 24 Jul 2024 16:35:10 GMT  
		Size: 51.4 MB (51370501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b1fac6edfc2c4ab8fe6d89745e9a6f9c89aff57d06578220b0b494c1350e9`  
		Last Modified: Wed, 24 Jul 2024 16:35:09 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3f8b6ccb634ae221e94e77f64a632759977ecc8eacb016dbb97f07be1d950`  
		Last Modified: Wed, 24 Jul 2024 16:35:09 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d543cb0d915bd2e7b715b394e03671cf8d9cdb9662bce828c212a73fb70e864`  
		Last Modified: Wed, 24 Jul 2024 18:17:12 GMT  
		Size: 1.0 MB (1023102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4cd30df6818908321ebbddfd68b9d92696569e8a6e4572ffc9636d117e6bd6`  
		Last Modified: Wed, 24 Jul 2024 18:17:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620f07a93fd8f85573ba640412f93a7031d634bd521c92a8b2c4c7eaa29618e9`  
		Last Modified: Wed, 24 Jul 2024 18:17:12 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92557c4b42e7e5ff5cd0c4849874fb960f36f2a4237bca9bcd48b465222e22c`  
		Last Modified: Wed, 24 Jul 2024 18:17:13 GMT  
		Size: 22.8 MB (22838652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb856b182616ffadb02cf2b78e90d8c34a74c19220da19f24f2cc1428e209cfd`  
		Last Modified: Wed, 24 Jul 2024 18:17:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:70bc9df03ace98921192d69506b94e3f534ee4a44e88d7aac6b19c619e7b81f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ac3ad6a0b03db8663ff1b170d253b58b0f3cfc35072c76fbcc62018cbbfad9`

```dockerfile
```

-	Layers:
	-	`sha256:ad57c1f64d81a34315cebcceb6731c82a0abcdca44f0b8624a6fd01304c2b74b`  
		Last Modified: Wed, 24 Jul 2024 18:17:12 GMT  
		Size: 30.7 KB (30682 bytes)  
		MIME: application/vnd.in-toto+json

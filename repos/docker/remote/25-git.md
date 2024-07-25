## `docker:25-git`

```console
$ docker pull docker@sha256:31fc20b6e060bc9a47ae1da4b0dbc2820749bdfbc044ee4f13f11845624464c5
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

### `docker:25-git` - linux; amd64

```console
$ docker pull docker@sha256:361fe73f3f3cb2380c8d099df994deea5e8a944caec2b9c3506b35391ed273f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128033276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050c0ccb70a301f2341f3dfbfdfca439a4b2878e995884dc31af1a9ad65c2f4a`
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
ENV DOCKER_VERSION=25.0.5
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
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

### `docker:25-git` - unknown; unknown

```console
$ docker pull docker@sha256:31be36ffe1b8555c8183aaddcdf351b9ce780a25c22b4022c19ce400e01b65df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876a5878b11b127f1084ad688e5cf5830a82689b306bd997819aa2953b77752f`

```dockerfile
```

-	Layers:
	-	`sha256:b467b2be29d610f4ffab522ac963c64daf2713c9f95d914d55f2680d14b0e90c`  
		Last Modified: Wed, 24 Jul 2024 02:03:42 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:162199dc1067370fa49c938f03ae77c9d34a774153faf10fe10255c395820ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120444527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8116e7d8d4a3f105ffc467c45267c5f0becaaebc5954a24d49a7c5308c54cf`
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
ENV DOCKER_VERSION=25.0.5
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
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
	-	`sha256:cebe1db06584e552d1517fc79b319f7dcea456486dd8eb3e5877dff02199a9ca`  
		Last Modified: Wed, 24 Jul 2024 01:10:05 GMT  
		Size: 7.8 MB (7799515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069f059ea230696f0d620fc14ea3366f2662d3c077645ba93b5b18637707ffc9`  
		Last Modified: Wed, 24 Jul 2024 01:10:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa6a997caf0928a0a534cade5a61dfe23ce2e435ae0b8f1ce1c10509ec44a9b`  
		Last Modified: Wed, 24 Jul 2024 01:11:07 GMT  
		Size: 15.3 MB (15274086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e221411a8f65c9d518e749396298fb590a9a610a3fedf115606f1f26554a1d`  
		Last Modified: Wed, 24 Jul 2024 01:11:07 GMT  
		Size: 17.1 MB (17117269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12d12b2b1708174575bf3947fff0f69913f4bd265be5d61c05a4149f52b9c9a`  
		Last Modified: Wed, 24 Jul 2024 01:11:07 GMT  
		Size: 17.8 MB (17776507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296de5a7239b69dfec20d12a609108835609db964afaa664c441178d97f13c47`  
		Last Modified: Wed, 24 Jul 2024 01:11:07 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b4961c11228301f126774e198501d7f6ba788eaac60205daff3b9c6db6a01c`  
		Last Modified: Wed, 24 Jul 2024 01:11:08 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2496eb9bb2b18a066decc82605958f64ce8fd9c457f6f49ab206042400aca022`  
		Last Modified: Wed, 24 Jul 2024 01:11:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa9f351d27bef806b055a68e71ec0c0020da718a3574534ead3f77a02de457b`  
		Last Modified: Wed, 24 Jul 2024 02:04:44 GMT  
		Size: 7.0 MB (6983518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38d33f57ee365a09803f841a2cd30ab0e30424414f96d80e7b1fd94bf1ae681`  
		Last Modified: Wed, 24 Jul 2024 02:04:43 GMT  
		Size: 88.4 KB (88408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b2c5401b0ea8d2d719ecd90a67db4bea5c37772bc12c69e6479e0fc92dd7f5`  
		Last Modified: Wed, 24 Jul 2024 02:04:43 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fdfe1eee19f4fe56ed4f427bfe98c53592370621daaf9b27694c2291bd23ad`  
		Last Modified: Wed, 24 Jul 2024 02:04:45 GMT  
		Size: 52.0 MB (52032079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff8be2cf02e6aa14cd35a068c2b0f3956b6a19d0be7ecc2cad74d3dd95e5df1`  
		Last Modified: Wed, 24 Jul 2024 02:04:44 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea15c6083030d45ad56777bfd7f788091a61b9f7a8f0583e551da306f57bf602`  
		Last Modified: Wed, 24 Jul 2024 02:04:45 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-git` - unknown; unknown

```console
$ docker pull docker@sha256:f8d6c838f6a6b8507563f873933c8874413eb1fa94c0b3ad6ab5c0100a4fd67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350b29edf27b41ceb90f3eb3f203e0ded20a98cc4e9edab584ccd06245a3d0c7`

```dockerfile
```

-	Layers:
	-	`sha256:55f82afa5191381b18a72eba51c9dd87fc7d0283f9a78b4e72b99a261c641731`  
		Last Modified: Wed, 24 Jul 2024 02:04:43 GMT  
		Size: 35.1 KB (35056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:8fec6cfe88ecc32ebea501ef9318480bab5d0b422a719568b81ef8ae54195117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118805691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc532e4e03a1ef9343def2a9cc13bbd000f9859cd52e6401742a18020c88502d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["/bin/sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
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
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8863baf0a8308f87f2abc52917ecdf2418c28292be1325eed43e77782c4e17e`  
		Last Modified: Wed, 24 Jul 2024 15:17:06 GMT  
		Size: 7.1 MB (7138057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e799e09164d0464b1fbfc400aee6a07962e530b4f4892416846be62c8edc931`  
		Last Modified: Wed, 24 Jul 2024 15:17:06 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e688148aaf226b56ab2237be485c06d37b5d7e2d34e02536f59162a296c4ad7a`  
		Last Modified: Wed, 24 Jul 2024 15:18:23 GMT  
		Size: 15.3 MB (15273175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579c5e0049c87f02db5e1f64a8dc16547a12de8779c8d6354cbfb157dda08c8`  
		Last Modified: Wed, 24 Jul 2024 15:18:24 GMT  
		Size: 17.1 MB (17104846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c8b689ec7cedc5e821c320ee67da3970f2b08bcdaeecc00bd52d49d3dd35c4`  
		Last Modified: Wed, 24 Jul 2024 15:18:24 GMT  
		Size: 17.8 MB (17762704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a993f3f9b613c87f6056a85f06284583d0dc19bcca1087bb7d1161df77f3a3`  
		Last Modified: Wed, 24 Jul 2024 15:18:23 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a589291fb69bb6a762ffa59d5f8f4b9476423d411e35f33d210db84d89f9eec`  
		Last Modified: Wed, 24 Jul 2024 15:18:23 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d948e64087baf7fc4f83ec5fc1990065d3a26fb05d791d2227a1f09f286ee1`  
		Last Modified: Wed, 24 Jul 2024 15:18:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de93dc2b655418b43989b1fa09786d7a680b048f765c691555a286e5666e6b9f`  
		Last Modified: Wed, 24 Jul 2024 19:53:47 GMT  
		Size: 6.3 MB (6307418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d21a0b5ce6bce00f0667b2742844e6310141f83a40bbda793161cdaa86f260f`  
		Last Modified: Wed, 24 Jul 2024 19:53:47 GMT  
		Size: 84.5 KB (84489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c16c2fe7d72305b88cde8f0151dd05a2dba524fcf1bc858f4fbd9b13e1a317`  
		Last Modified: Wed, 24 Jul 2024 19:53:47 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95601007189841625ba669b4e9ebd1577667eb6067f32a60de2cb3c794b9548d`  
		Last Modified: Wed, 24 Jul 2024 19:53:49 GMT  
		Size: 52.0 MB (52032098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fa56a6a1c018a38d0e4dfddeece7ade78a6772ffa3817c49cfc576a021920a`  
		Last Modified: Wed, 24 Jul 2024 19:53:48 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c913802c630688d40495e10e16e4985b1dea6ff25b2c09dcb3a6f792519f78`  
		Last Modified: Wed, 24 Jul 2024 19:53:48 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-git` - unknown; unknown

```console
$ docker pull docker@sha256:9eaf5f2462e44f4d374969434ae6d8fa0a9c0aeb294b05cf9a2f7e8ab5ef9f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd65ea275eb9491262aa375e86435b42016f2c6cc4169f48737691c8471834c4`

```dockerfile
```

-	Layers:
	-	`sha256:661ea6db2fc9789603cc101a6cb7bc91f4de36e5ca6de507f211a1418074c210`  
		Last Modified: Wed, 24 Jul 2024 19:53:46 GMT  
		Size: 35.1 KB (35056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:63548326111350dd837cc3c27aaa54771c0d8dc3fa8b970b619c1bceb9c08f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120435490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24177a9e191dd58d4f083e42b77e98aae6a77a436449799d0660a1966d36c4b4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 19 Jun 2024 00:17:01 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Wed, 19 Jun 2024 00:17:01 GMT
CMD ["/bin/sh"]
# Wed, 19 Jun 2024 00:17:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-amd64'; 			sha256='62c2cb471c765b48a2b6fd0c09c8149b789695eb631bc1b7b60c047f75907f3f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v6'; 			sha256='e8092bdfe77337b27d963d5a0090b7be73e293e1c59ff0ceaac560b749fe42ba'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm-v7'; 			sha256='8acad24cbefa6e8614c55fed2ac5c822303647563a4e14019eb9e8907ac02b5b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-arm64'; 			sha256='024f62e6bcd20d29f9ab45ecb49963f93311991465dddc62b8d8a32443aa36ce'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-ppc64le'; 			sha256='328dc59f720f59aef58af35af3202a479bac7ccbb8c02fd9db60e8dd4561a2a1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-riscv64'; 			sha256='2f6a0703e3359395574621a071896d02ea4240570813a5ea154febbe6d39fba0'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.linux-s390x'; 			sha256='3423d552b0ed13538890b054cf5bc1605a396f77ef800a9a8192024cb5e90230'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Jun 2024 00:17:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Wed, 19 Jun 2024 00:17:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-x86_64'; 			sha256='5ea89dd65d33912a83737d8a4bf070d5de534a32b8493a21fbefc924484786a9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv6'; 			sha256='5fdd0653bb04798f1448bd5bdbecea02bcf39247fcc9b8aab10c05c8e680ede0'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-armv7'; 			sha256='0d675f39b3089050d0630a7151580a58abc6c189e64209c6403598b6e9fc0b21'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-aarch64'; 			sha256='7f0023ba726b90347e4ebc1d94ec5970390b8bddb86402c0429f163dca70d745'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-ppc64le'; 			sha256='9d69aae252fa7fd3a234647951b2af496ee927134d5456d4b8bac31d4d260f5d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-riscv64'; 			sha256='91b6b2f56e8cba3965a5409fa5125d3f01408c9b2d0bf5b9c119f353601d1e51'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-linux-s390x'; 			sha256='1ea22d04bab9452de3169e22b60d77a232acdf829ac4858dc780085dd7fd4c48'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
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

### `docker:25-git` - unknown; unknown

```console
$ docker pull docker@sha256:1299fffd009debece10b586ce6be3c9aa8831f5c89aa650b2f1779dd3046c902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 KB (35341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f771181113fa03489eee585bdae70f435b8d50e61fce76196cc1543c888f83a2`

```dockerfile
```

-	Layers:
	-	`sha256:a76ca0cc4a20d79750c626bdce9be5ba9e22b3f7f4380df83dc1f6bcd847f7a8`  
		Last Modified: Wed, 24 Jul 2024 16:35:08 GMT  
		Size: 35.3 KB (35341 bytes)  
		MIME: application/vnd.in-toto+json

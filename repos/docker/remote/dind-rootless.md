## `docker:dind-rootless`

```console
$ docker pull docker@sha256:a85bf1d09cf0c684d7de3268d4c54b8bb152b79b53c1efa324cc8df94da42b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:5b34a2411903326499d2f67470d83ce97dc0183ca802e6fcf91ca1b564bf01bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154153776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e83a23dba859599f0adfa4a4b7996f23a41de2f5621f047074a9da77c6274f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db09d90694836eab5370b7d5f552b34f5772781701b00fd4e7c3950519ee72`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 7.9 MB (7872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538dd9aacd297989031c915937096bfdd889838bf150c05212223a9b3507070`  
		Last Modified: Wed, 11 Sep 2024 02:01:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfaa9e1957304899a8d16f9cf6fca1ddbf8debde833e6b68831a81b50ee6fc2`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.6 MB (18601177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616c0277b4c4b06061b57f23022504d07faea54188b3a5b0d5b51dfa4e990b9`  
		Last Modified: Wed, 11 Sep 2024 02:01:55 GMT  
		Size: 18.4 MB (18432770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692e2842ca25a9bf245905f6e29b66a65bbdc85f1873aae896b69370566a5f9`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 18.8 MB (18825278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cd67bc2f21b34aeca4c5627b6b4b5dbede9b76ea404dd4079e77464166d0b`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4966ec96386506904d07991e403853675dc204da54a5e1fd0c1abd1e6da10197`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1d01552a20f6313745d5d6563fc8a44c75d0010cb7cd94399a1487838380`  
		Last Modified: Wed, 11 Sep 2024 02:01:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c62cf5a0b55f78c6952456f627b45a4927bcd20a476a84feebb376a2e5afac`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 6.7 MB (6657921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3592c908208e8a16c99d3263902c97301ed446b46205bfcbb8d9ee8611123fa`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 89.2 KB (89218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4c1986daa1bdd24f3621084f644cff84734eeb7aff037024fdf56f6aae3c1`  
		Last Modified: Wed, 11 Sep 2024 02:51:00 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f41134be18ef5373326b3114ba85c9698be27a64dc12f0f60a1f5e6d0eac9`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 57.8 MB (57773398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eaea47f5e1a31cc71bc565396dc93187e844d7f4ad7885746889e44dc40a4b`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a6f212eac3af392a8a5097e434764cff04c4e70ff2a9c1d4809c5c2e18d9e3`  
		Last Modified: Wed, 11 Sep 2024 02:51:01 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b065473b42eefb9a792eb005311c212c14df916c2575869263ae2fc25bd862`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 981.0 KB (980986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852d28940731d27787147baf692114c5a57e84af5870515a9cf826785e61c97e`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2754af7f7c8de794edb28a5c9f9ba8c90bdf84c274b9f556a39c0ea3240f1ab`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636b57c4498bf4e949f7e09044a06c834e167dc3facda3697e3e1fff4b1739e8`  
		Last Modified: Wed, 11 Sep 2024 03:48:50 GMT  
		Size: 21.3 MB (21287315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f993cc096d161b79e4c922715fa6fe0c3d065ffa32abe11cf805a5937def91`  
		Last Modified: Wed, 11 Sep 2024 03:48:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c3fb49a3f69e9f44f3a3f159a35777da8859fb3530256aa2e196c953dfb4f8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7759138f227c5ac9b927aa368e0931f67ea0cd6196dfc9785aa8c3d4a23bacd`

```dockerfile
```

-	Layers:
	-	`sha256:7fc1f180c7e9851ada027667060ef9f9afc83a449caaccc1e42e3f58de86ba7d`  
		Last Modified: Wed, 11 Sep 2024 03:48:49 GMT  
		Size: 30.6 KB (30580 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bcedcdbefd4c0a8026ca435140dd2260a8b8de76d7f7ca5aa88030b661852828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148310987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d21859101d6a92e4bdb3cd0fc0396aab45b56110d1c29617704bda32774c45`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_VERSION=27.2.1
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-amd64'; 			sha256='6c65b3a80fd65312ed4949b76d10077c304ea013e78251a91cb0990562ee82a6'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v6'; 			sha256='e7236f91db70ab596cfa2ecd9f05c8231d18aa8da6fffd3439d69b5b04002e81'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm-v7'; 			sha256='e6950b2551f9930dd9894504da337a978c36052cb3517af63b4f65483364e70f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-arm64'; 			sha256='8a971c4c9019f646fe9ac73c7e1cc3593a1246d43ddd9da24c588d1d93ca4c4e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-ppc64le'; 			sha256='73fa298b089705b0420ae7cdd6f7859b9b2d0ab157d9dbfff70cffffe6f1e8a8'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-riscv64'; 			sha256='e7f5d0ac2d1c24d187e678f1bc40a55ef99bf04da7947d1901efa5bfeefc6869'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.linux-s390x'; 			sha256='1f97a8bc3bf91f0aded613adcf8115e8e9319f0d69dd912ba4712bd22dbd3f51'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.2
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-x86_64'; 			sha256='d037bd4937bf18fba67cff4366e084ee125a3e15c25657ee1aeceff8db3672b4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv6'; 			sha256='7c87109062b62da7433fceb40fabc1049060d6c594894f25ab5a4a1b8289848b'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-armv7'; 			sha256='75b2802a11277e193cb0998d0830e89b3fef28b15b66c71a7d489173db675486'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-aarch64'; 			sha256='1caa6c39b9df88dbd8522403d78b786a4151fa4e881c866725f75b5d99500a9d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-ppc64le'; 			sha256='15dcafcfb773c56891fbba94151f86a65eb0f697ae5976fcdea71c84d58d4476'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-riscv64'; 			sha256='020b2500320335c3a043deda632dc811944b4e683ba1c50e1cd8917b540e01a8'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.2/docker-compose-linux-s390x'; 			sha256='32930ff623836bcd87f1ff4c271daf1af93ce2246785fdd24076ef7d91505b43'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD ["sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 09 Sep 2024 11:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Sep 2024 11:04:22 GMT
CMD []
# Mon, 09 Sep 2024 11:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 09 Sep 2024 11:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Sep 2024 11:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c72c1857a6742cc744af6963182de9c3e7800ee987dda507c381112a5f8f57`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 8.0 MB (7981921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d086486b1ed82764b6a71b1ee004f6da3c9b4c55822899a96c323b2de2cb8`  
		Last Modified: Wed, 11 Sep 2024 02:01:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c78a57c063a9094aa00fe6bb46d4acad86c98f6a3d2049f34485ec091e1e05`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.6 MB (17556297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc32acba734d5aee4c79744637d20dbf08a4fd51571a9afd37daa5fd685218e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 16.8 MB (16799661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eada7f8d96edf35fbf9cccdfe2a31683f121351212c1d270f7a73b2e1f530e`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 17.2 MB (17186842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b544e07d92af2d47cc10db55727317ca8ccc95a899db6ce41cdd41cb820c0`  
		Last Modified: Wed, 11 Sep 2024 02:01:35 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ca207ff0f9c918c07b12825084dba82e9f8c9d490f1ffcf33fe0c7b45fab2`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718c5493b785a7581afc20e1db4ba86a79bd5e5e8ef3dfa1ad64620028e196eb`  
		Last Modified: Wed, 11 Sep 2024 02:01:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5be9720db99d659c53b6a67a1dd2ba6e958b7622248ab8dfc91c58d5c0f1d`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 7.0 MB (7034910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bcabad1025e90ed07d105bd2724f1565672227ec5927061b082183adc6b11`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 98.7 KB (98650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9235e7f34f8cc28423dac4653e318c60d54cff3b0544a5e924074efdf31578`  
		Last Modified: Wed, 11 Sep 2024 02:50:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d4c07d55e9442550b66fb78c2d91de8856309dcc6875aa4c34aaa96f85316`  
		Last Modified: Wed, 11 Sep 2024 02:50:50 GMT  
		Size: 53.4 MB (53398203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df4284aea7cda8255fd5026391b9b8b9db9af96da9875fe9db8f0185ac0ccd`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c51f22e855b132e7146b336aac0310cbe52e537cd77af861d9f27629b425ea6`  
		Last Modified: Wed, 11 Sep 2024 02:50:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61abcef331c5400bd552a2b6a5ecc6d03ecee4f12e9cf72c4a866ec26c4e2fe7`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 1.0 MB (1023119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0a2f42af77b9a719e519573af0f3e531e92847a4b6f6095d42ffb21b48ae44`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d713d1485ac825869be3a208d8d2699337d7ce096e81e2eeab4f7fc83fd0cc`  
		Last Modified: Wed, 11 Sep 2024 03:48:43 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c70f1919f2604484b0212c929c9881df57425101e48ec186fc604ca7b74c92e`  
		Last Modified: Wed, 11 Sep 2024 03:48:44 GMT  
		Size: 23.1 MB (23134441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab61b3f82263bbf4714ce5dc1a9816f6c16b3a159cd8e8cf873a94ce857aaeb1`  
		Last Modified: Wed, 11 Sep 2024 03:48:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0cdb6cb36b46b803fec1343b539275b39b36043f1df4e6fd6c3dc696980ca15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4a5c6803fcd314f69e271e0c35c18f4c05e2f48eaf0c977c298dcc6a732c71`

```dockerfile
```

-	Layers:
	-	`sha256:e6bc659420a6a66c2ebcb45c47ea7e01bff903c946a478d6fe5246ea077cdc54`  
		Last Modified: Wed, 11 Sep 2024 03:48:42 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

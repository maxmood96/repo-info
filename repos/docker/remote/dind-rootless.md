## `docker:dind-rootless`

```console
$ docker pull docker@sha256:10f4d8fc4ae66960fe350c3e18bc5d8bb9d26b27322dece040b550b9290666ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:67e92eba86182779205c29d041d8fb8c671919211becdf7eb6653bf511bf18ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151939251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b1ec278e4fa3d01c5712d1b6bfb4c8ec8f70f15ecd9f0610cb8430f56c446`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 05 Jun 2024 18:50:46 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
VOLUME [/var/lib/docker]
# Wed, 05 Jun 2024 18:50:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD []
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 05 Jun 2024 18:50:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f545e3e1f00b5bce8b95fd91aac5c0f51d4bc510ee81eb18f2b28d0475b4a2b`  
		Last Modified: Mon, 24 Jun 2024 22:56:19 GMT  
		Size: 2.0 MB (2010478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5046d34b4c897d93939d5eb8891ad80e998ef0a6068d5d7fe47c4d637c9dec08`  
		Last Modified: Mon, 24 Jun 2024 22:56:18 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdbe6a68098b960cde91d6fc57b771d1992a79ff072ba7d95b0e3b437204392`  
		Last Modified: Mon, 24 Jun 2024 22:56:19 GMT  
		Size: 18.1 MB (18054136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcd3a662cbab32066346fdb2d4f5c1de0cb01b19393d8e7c2f4a0f0c66be020`  
		Last Modified: Mon, 24 Jun 2024 22:56:19 GMT  
		Size: 18.2 MB (18178848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d3515815d8207a17518ec6ba747202d879f4f44b053d217244cc6fa2b29522`  
		Last Modified: Mon, 24 Jun 2024 22:56:20 GMT  
		Size: 18.8 MB (18792463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73af0ccfc8a8605ba48753bca231c17d8e4fe1def0f14684cc6cb163eb1e938b`  
		Last Modified: Mon, 24 Jun 2024 22:56:20 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2eef97f206ba1155f61f0f9351729451a9345eb1299614901e33e383c85c7e2`  
		Last Modified: Mon, 24 Jun 2024 22:56:20 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97148ec656071c0f97aeb0210812d1009ffa6211d6372586ef474a3af6a5fbe4`  
		Last Modified: Mon, 24 Jun 2024 22:56:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22198c6c7227f2ad5eca22e1cf01340221c458347471f04c0ff79df9a9e4c21c`  
		Last Modified: Mon, 24 Jun 2024 23:57:49 GMT  
		Size: 12.5 MB (12504425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7aa5afcdfa1892566d67a14646a76a6118183c87e72973a4da14c0b84a6de7`  
		Last Modified: Mon, 24 Jun 2024 23:57:48 GMT  
		Size: 89.2 KB (89184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a199671fb3e9f7b4e9aa700ea0ad5ef5e231628fa1530456c7d40c34d3765e8`  
		Last Modified: Mon, 24 Jun 2024 23:57:48 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dd0319341eb35f3e2ad272219ee7062d2e0fa4d906d146dc8d9e43135ef4ad`  
		Last Modified: Mon, 24 Jun 2024 23:57:49 GMT  
		Size: 56.7 MB (56713249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e36963586b841c6b7b66a32677fedb82b16e36a87dc8467e090880756b7ef2`  
		Last Modified: Mon, 24 Jun 2024 23:57:49 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692faf0fc7b1ace8d80c89c0e033d4e0f47f8bf25b43d94b5b141f3ad55727c8`  
		Last Modified: Mon, 24 Jun 2024 23:57:49 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9abc2a33de99f366cd813ba441c25f7e4045b215deb62bddc909ae642e3467a`  
		Last Modified: Tue, 25 Jun 2024 00:50:15 GMT  
		Size: 980.9 KB (980945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a966d8b4cf38b01f37b5c65331b53519088f76018fc744d8889bac600d99105`  
		Last Modified: Tue, 25 Jun 2024 00:50:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bed9f3e0ee2c37fbde9959b267e14081d6e598c4de362160a3f66955b3a3a0e`  
		Last Modified: Tue, 25 Jun 2024 00:50:15 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16941119bf026fb14bbd83e44c5c1102bdf369848c1689ef741ad75068446343`  
		Last Modified: Tue, 25 Jun 2024 00:50:15 GMT  
		Size: 21.0 MB (20982366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56603b0994fbf86287cb8fff2cd819bcba2819d8807ca720ad50806a5da58e05`  
		Last Modified: Tue, 25 Jun 2024 00:50:15 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6cae2cabdb1677d8ab5f44f23cd73277a8de7995263a6ecbd1f4b3f71c3693e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42661f6467eae050330c373ecc51813a06f94d8a3c91e54b59506bac6af3d9f0`

```dockerfile
```

-	Layers:
	-	`sha256:14cf482b400121dbb43e5ddd9b2dbea939389e68ab24f8a2eb616b8ea3e8f782`  
		Last Modified: Tue, 25 Jun 2024 00:50:14 GMT  
		Size: 30.6 KB (30585 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8781681029ccdf64071313834132c4a9c024e03a44b7b959039328d1236dbffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146151545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31aa23b208ff53cfaab5c9e3f48190a22e02fd4744d880bdf247101a75ae809b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Tue, 25 Jun 2024 11:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
ENV DOCKER_VERSION=27.0.1
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 25 Jun 2024 11:04:53 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 11:04:53 GMT
CMD ["sh"]
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
VOLUME [/var/lib/docker]
# Tue, 25 Jun 2024 11:04:53 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 25 Jun 2024 11:04:53 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 25 Jun 2024 11:04:53 GMT
CMD []
# Tue, 25 Jun 2024 11:04:53 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 25 Jun 2024 11:04:53 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 25 Jun 2024 11:04:53 GMT
USER rootless
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b7d7f194b09818411861e5ecb7981b06eb6b3ec9567d305a8ff61126b59696`  
		Last Modified: Tue, 25 Jun 2024 22:59:12 GMT  
		Size: 2.0 MB (2006626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f451447f796e33222a762e38d9f0f1adc095908e0471fe0f2d2ba1e6df653a8`  
		Last Modified: Tue, 25 Jun 2024 22:59:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10443691cf32df9a005f50e6e749276443f481c527db0edae30a3a48c539f2f3`  
		Last Modified: Tue, 25 Jun 2024 22:59:13 GMT  
		Size: 17.0 MB (17033101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa1358c112321b88760b238ad2cba6806fdc792864aa578ad85ed53d87b138a`  
		Last Modified: Tue, 25 Jun 2024 22:59:12 GMT  
		Size: 16.5 MB (16538019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdde108f195f06555d6d665eec5854888684c6c7fb1300044a7ca0d93cc02ef`  
		Last Modified: Tue, 25 Jun 2024 22:59:13 GMT  
		Size: 17.2 MB (17151897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae419d2259936fcd98d4f2737145a3c5f8c187c12ef560bb9ee984571640866b`  
		Last Modified: Tue, 25 Jun 2024 22:59:13 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1709b39e7ba9ea7c39752a72d64ac09a6f4b4846db8105658f6ab0946e3d8d92`  
		Last Modified: Tue, 25 Jun 2024 22:59:13 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d9b1889fe3f12d5c56966a0bfdf33301e3dfc5d8f92ca509c71adc4e888a05`  
		Last Modified: Tue, 25 Jun 2024 22:59:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720f1db049f8ee683a8f1901988fa08e4c25906e5b75288cc0d1fc24888f74a8`  
		Last Modified: Wed, 26 Jun 2024 00:43:55 GMT  
		Size: 13.0 MB (12991249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48d24216397d368d5a3816905b41f4e92606a2a0f06e654e32dcbd108635e98`  
		Last Modified: Wed, 26 Jun 2024 00:43:54 GMT  
		Size: 98.6 KB (98627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf24783d687b0074aefed91d1ae33007fc281f9d67685f318b040e7dbc18653`  
		Last Modified: Wed, 26 Jun 2024 00:43:54 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb29a7d894eb16f77566ee68dad7d60d77ad8f77f5c64c98bf94cc0fa77b06ac`  
		Last Modified: Wed, 26 Jun 2024 00:43:56 GMT  
		Size: 52.4 MB (52373873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e38ba2a136909bd78ffd4d8f59303f59eece7193697abbff002c9ea6c7ef80f`  
		Last Modified: Wed, 26 Jun 2024 00:43:55 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04aa82efead2ccef451e94780538d3e4689bdb45f91450ec54bd7f20a416ac8`  
		Last Modified: Wed, 26 Jun 2024 00:43:55 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dff7ddb0324e1bbb834b650c0437cec877559232192e7397ef975be4919177`  
		Last Modified: Wed, 26 Jun 2024 01:36:50 GMT  
		Size: 1.0 MB (1023093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d358be176211f292fceaf545844d235345e5b4d7c728f47268e0b16ffcc472ea`  
		Last Modified: Wed, 26 Jun 2024 01:36:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68ea967b5f22986baa5d01d615bc9eb73b288e3f6f99f4a129d077bb470799f`  
		Last Modified: Wed, 26 Jun 2024 01:36:50 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf601c56d1a01cc8e7c719c011ce3b8fde724999c86a036914a9ca6717d8e24`  
		Last Modified: Wed, 26 Jun 2024 01:36:51 GMT  
		Size: 22.8 MB (22836941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a58b1e1d2b0c34bb33643147662053119916d5cad8d2fe29e3a943634d4de3`  
		Last Modified: Wed, 26 Jun 2024 01:36:51 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:eaad7111e378fa3e3225748ef1448200e416a13ae8e8500ff261ce4807d83892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607713f145f23b0439c534efb987fab5f2560fa5ffe048718592db62f8916836`

```dockerfile
```

-	Layers:
	-	`sha256:ccd5f637f0b38d963f48239df2c7a31d8d606c9d049a638d747c30b4ee11066a`  
		Last Modified: Wed, 26 Jun 2024 01:36:50 GMT  
		Size: 31.0 KB (31011 bytes)  
		MIME: application/vnd.in-toto+json

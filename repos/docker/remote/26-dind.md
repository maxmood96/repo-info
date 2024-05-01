## `docker:26-dind`

```console
$ docker pull docker@sha256:56e2c522194d81689c2787c76304777199cbdc741d7dd798d06e33967361d92f
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

### `docker:26-dind` - linux; amd64

```console
$ docker pull docker@sha256:8bd6302a909f6f2ed9a17058cce2d83442bddb9e65c974352c2ba485a1e6d7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131465552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd8081463dacc456f31bdcd773e7f1ad8954592ca1a3052a164bd3f45ef3ca3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_VERSION=26.1.1
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 30 Apr 2024 17:04:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
CMD ["sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
VOLUME [/var/lib/docker]
# Tue, 30 Apr 2024 17:04:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 Apr 2024 17:04:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f1d5d472fe15223da6e43b59ce342f0e98d80664562b2a2b14259f23862f5b`  
		Last Modified: Tue, 30 Apr 2024 21:49:48 GMT  
		Size: 2.0 MB (2026154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd324c58b14eee17de7e63a209be9a6b28cc90f05ef54a2abfee462a2051012`  
		Last Modified: Tue, 30 Apr 2024 21:49:48 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560af3c6f801629d1eab1b09a057f80c8a9516cd70ebfbfecaa0bea2a3f8f62e`  
		Last Modified: Tue, 30 Apr 2024 21:49:48 GMT  
		Size: 18.0 MB (18023175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d56477ff9db9738ad3a1e4028529cb140cc263449b4da5dd347eb519c8c3ae`  
		Last Modified: Tue, 30 Apr 2024 21:49:48 GMT  
		Size: 18.1 MB (18078213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e17c23668a49531c2bd081e90967fef76f57d1d981b5bdb4c28aaefd19e4d4`  
		Last Modified: Tue, 30 Apr 2024 21:49:49 GMT  
		Size: 18.8 MB (18764669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef3cdaccec305bb0cf40ecbdc31d2f48f6ebb223beb6fad36272cbd1904f60b`  
		Last Modified: Tue, 30 Apr 2024 21:49:49 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c82127e9726872164eeb8dd0adfa8042361456cb1ca0fc559bdb592abfd60d0`  
		Last Modified: Tue, 30 Apr 2024 21:49:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a53779d90e189c1ef9fb0d61a8417cabb02131a963fe7608e99676bdeab4160`  
		Last Modified: Tue, 30 Apr 2024 21:49:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4b2e0e92ab08c1a1fb17f05b6f2cf0f83b57caf6f72830bb2e095a60f9e8a4`  
		Last Modified: Tue, 30 Apr 2024 22:49:27 GMT  
		Size: 14.4 MB (14355035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04c06bd741289c7ec3b467a7a7791016190fae551b8104dfd9c7e34e69e0208`  
		Last Modified: Tue, 30 Apr 2024 22:49:26 GMT  
		Size: 89.1 KB (89141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6e76308ff3d85e18792a19bb7b92574c5d2663701c4b14397307e36641ec98`  
		Last Modified: Tue, 30 Apr 2024 22:49:26 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1654052352be998bec978b87c922d5b31bec994e7a60b6d97a802c734409f25`  
		Last Modified: Tue, 30 Apr 2024 22:49:28 GMT  
		Size: 56.7 MB (56712113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3770e5ba44ad946fb5f18e81f9a3ed904be4423f4585cf4317636052fdbfa57c`  
		Last Modified: Tue, 30 Apr 2024 22:49:27 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a945827fa8835fc597b56f5b1dabf556d703774054a8496238fac7228d7aea1`  
		Last Modified: Tue, 30 Apr 2024 22:49:27 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b15de119029a6030f72178fa4ebf8efaa1907cf065497aa037c81c7fc808debb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.4 KB (865429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca35787404c118d706c5063fdca8ce12e856fb5c46795e04e9e4cc65c1adc457`

```dockerfile
```

-	Layers:
	-	`sha256:5ec1f9bb8d20d5942611c896372d11560af5bb885699bb874641b84a0954a7ed`  
		Last Modified: Tue, 30 Apr 2024 22:49:26 GMT  
		Size: 829.2 KB (829172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed219977392b7305569960192e19714a8e635527e130bcf48c1357c4690c8982`  
		Last Modified: Tue, 30 Apr 2024 22:49:26 GMT  
		Size: 36.3 KB (36257 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:eb8eb3f510834cf2cff8e8ad96f22f5eda94867493c90af89028afb9fb69ef7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123650594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38819780b5212a13963c2c546429d217809718c58e4857f8e1b8db6fbe721137`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_VERSION=26.1.1
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 30 Apr 2024 17:04:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
CMD ["sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
VOLUME [/var/lib/docker]
# Tue, 30 Apr 2024 17:04:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 Apr 2024 17:04:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
CMD []
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0b230aad35f2b78ce4e1ec560de2a832387672d5c9b4315323ea10891ba2a5`  
		Last Modified: Tue, 30 Apr 2024 21:53:20 GMT  
		Size: 2.1 MB (2116779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574d227c87acd211ab67ad21e6eccc838099ecd4a9bc05e5b7a30342bf114f0`  
		Last Modified: Tue, 30 Apr 2024 21:53:19 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f52789929cb96ca51f82d607016d836f188edd2bc60fac7635a76b425c4604`  
		Last Modified: Tue, 30 Apr 2024 21:53:20 GMT  
		Size: 16.3 MB (16316721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230ce9b3c872cfdf2a05f8742977c1653e259294ebd3de9058e35254077b24b9`  
		Last Modified: Tue, 30 Apr 2024 21:53:20 GMT  
		Size: 16.9 MB (16915879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46936893ef39e45bd39ff16095c9fd6f1916ea0216e469a21b944c1f1fa589dd`  
		Last Modified: Tue, 30 Apr 2024 21:53:21 GMT  
		Size: 17.7 MB (17726576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cab2e4ad789d0afef8aa63050e5446a8dbc9f722b86e307c5357ab58772e1f`  
		Last Modified: Tue, 30 Apr 2024 21:53:21 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc07b9b264c1e8db63eaeda431ed3508bda55e4ff4735a0a4a4e0962ff3ad499`  
		Last Modified: Tue, 30 Apr 2024 21:53:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b83fab74de503313dd1ba1d8a6f8702ffe5ea2cf8e0c97f41a90ca17f51e32`  
		Last Modified: Tue, 30 Apr 2024 21:53:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dda5ce5889b88d1ea9dff28f5967fd9e545a0271beb8e5825de7691041fa85`  
		Last Modified: Tue, 30 Apr 2024 22:53:46 GMT  
		Size: 14.3 MB (14316683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c876f0bc2615267ba230f6eb2aaf9d08f1491d414786fd79a9ff01984429c990`  
		Last Modified: Tue, 30 Apr 2024 22:53:45 GMT  
		Size: 88.4 KB (88364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcb59937b7a422467f0a87ccbb90e8ec9d737ac8b8dbf658d15645691c5409e`  
		Last Modified: Tue, 30 Apr 2024 22:53:45 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee0bfcf48d44474795e7b5f4cce5bbc4893f316feb9b22d89e054cbaaa2248e`  
		Last Modified: Tue, 30 Apr 2024 22:53:47 GMT  
		Size: 53.0 MB (52995869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6167724af31580a11840b86f435990e073ebb9402e6c34fb659cf0057b200dd4`  
		Last Modified: Tue, 30 Apr 2024 22:53:46 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c318dcd9addfc7aef40009cc999ed428bad430dd1b699af21400c305ac4526a`  
		Last Modified: Tue, 30 Apr 2024 22:53:46 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b07b22a7c50b312f814817c8308da87afaae64f43e32afe8c9e794f0939ffe1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 KB (36261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d739279d34301fb93edf5e1eb6afd63b130585d0863cf5461c22feb71d37416c`

```dockerfile
```

-	Layers:
	-	`sha256:2dafaa9ff2c64fa9f2114092997f70e4cbd51d2b25bc62cd30a28220861d08df`  
		Last Modified: Tue, 30 Apr 2024 22:53:44 GMT  
		Size: 36.3 KB (36261 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:bd14619c24f1dc5dc4a68ec6f484b30183d95fcb2a4d5e0d8ef9af61a4418390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121854322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e39a5fd08e3446ec15eaf6ca2a3ccb105daeb43f60128698bd9dada5e6824e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_VERSION=26.1.1
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 30 Apr 2024 17:04:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
CMD ["sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
VOLUME [/var/lib/docker]
# Tue, 30 Apr 2024 17:04:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 Apr 2024 17:04:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62203ebc003cf77a4ff92a3c67a89cd14dcf1adf84fb125d2f3329ad08ad9a61`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 1.9 MB (1896160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8418dd6a88f431ade9efd4277500a4c6483d9ac98459ff95a86dbfde7d02e2a`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e2653da14679cfb0a8eddcb755883e0a705fe3e5b98db684ca67214185b368`  
		Last Modified: Tue, 30 Apr 2024 21:55:44 GMT  
		Size: 16.3 MB (16308957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd1168a48c947a0af62ec3ff5c1125165b2dcb86aae2f5e3884c668716c7b72`  
		Last Modified: Tue, 30 Apr 2024 21:55:44 GMT  
		Size: 16.9 MB (16901914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c74aeaf0ec4420a40bd73fcb89ed96386fd33f0d3daf0c137ff72397b62424`  
		Last Modified: Tue, 30 Apr 2024 21:55:44 GMT  
		Size: 17.7 MB (17710686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc77c003f0ee7e0981cb46480e88838b6d827004e54ce53d5490ac5589b6b7`  
		Last Modified: Tue, 30 Apr 2024 21:55:43 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a8dd3735136a6bcc4749d4ceb777f060e485f5f8f2e71f3d9c81873b4a0f3d`  
		Last Modified: Tue, 30 Apr 2024 21:55:44 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd7c434e06f9070e3827409cb1d1110455a65a3bad56fd12bb7a425559012c3`  
		Last Modified: Tue, 30 Apr 2024 21:55:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcb62a5491eae429f8ab6c3b0bce4a3e9de819f43e2c970c288027c66a56cd1`  
		Last Modified: Tue, 30 Apr 2024 23:03:45 GMT  
		Size: 13.0 MB (13029224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c69279988eb9e88d402ef0cff784659064f477aaa10a570a7a0019a619f712`  
		Last Modified: Tue, 30 Apr 2024 23:03:44 GMT  
		Size: 84.3 KB (84285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6efc591aeef5e818eaa408a52ab48c29a7b5c7cde1ad9c0da5fec4d063a970`  
		Last Modified: Tue, 30 Apr 2024 23:03:44 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2ed235e4a6253b3e797dba5b7d8eeaa5d477c84dbe49fbc2e40d7a1221f587`  
		Last Modified: Tue, 30 Apr 2024 23:03:46 GMT  
		Size: 53.0 MB (52995875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101c63522e2bd4194a7f688c25b2f2b1b8ce2bb82c15f3cdef93f7d7b8600a3d`  
		Last Modified: Tue, 30 Apr 2024 23:03:45 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1657626bfb678d968ff583be8a35da5779d3054263a499d33304921ae0b23434`  
		Last Modified: Tue, 30 Apr 2024 23:03:45 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind` - unknown; unknown

```console
$ docker pull docker@sha256:03a646227eae7ad9a7e85e3ef8f4b943c4abd9edf1c88aacf7073d809e202900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **862.4 KB (862420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506d4f82fd51b393cddb63bd33a9cf18264667001e8c0c02fa3cf0958f23095c`

```dockerfile
```

-	Layers:
	-	`sha256:b2b3aa276f5baa17a7207b9656dad8caf6a1c72aaccaa693a09cd8f3044f5d9c`  
		Last Modified: Tue, 30 Apr 2024 23:03:44 GMT  
		Size: 825.9 KB (825939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0e7d3750e1d4e9bfc1dbdcb6fae3d364c6940304ba36b4f6b22f9b8abec7945`  
		Last Modified: Tue, 30 Apr 2024 23:03:43 GMT  
		Size: 36.5 KB (36481 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:501b82b654f0a616a5166ac7be03ae5cabac471e5c286584c2b76b9f29b9dd14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123073166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034eca08de42249cbb9f86a2349f195e591482fd27b28b5867c56d52373c7f17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_VERSION=26.1.1
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 30 Apr 2024 17:04:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
CMD ["sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
VOLUME [/var/lib/docker]
# Tue, 30 Apr 2024 17:04:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 Apr 2024 17:04:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 Apr 2024 17:04:38 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d7746a1a70eb44705adb69dc7142560a26f83aee9219582321bfab31455acb`  
		Last Modified: Tue, 30 Apr 2024 23:14:26 GMT  
		Size: 2.0 MB (2027968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca9c9e8e89a3309c5271493837dd27775e44e4c2fa505bb789d4c941f563107`  
		Last Modified: Tue, 30 Apr 2024 23:14:25 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54db07621a4752aa55af948a121c961b4a88d6a1d57a5a28c4c2158b74a3dbfc`  
		Last Modified: Tue, 30 Apr 2024 23:14:27 GMT  
		Size: 17.0 MB (16979595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f293e543ce605185c12e46bec2efbf24f52b436b82c211c95feacdb4ca56693`  
		Last Modified: Tue, 30 Apr 2024 23:14:26 GMT  
		Size: 16.4 MB (16441656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f110dd69412896ed2314b0729e1b3469667f391716b1e8ca50c443e558ca14a`  
		Last Modified: Tue, 30 Apr 2024 23:14:27 GMT  
		Size: 17.1 MB (17134317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf75382e81690f84cd7745f4464071f3a71fd4b713ff817e868b240ccbb0e1b`  
		Last Modified: Tue, 30 Apr 2024 23:14:27 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5a53d628353f7ef1bfbb9ada3b31357418596609be94d39743add2ed527789`  
		Last Modified: Tue, 30 Apr 2024 23:14:28 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a7fd3044e3680c3de23fae840e1e9f53121640829e4097f22ef2c85da19842`  
		Last Modified: Tue, 30 Apr 2024 23:14:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce12be87b465fa1dabb5f1da9b48cbee9d2cd762a40a4b9f6f6079582ce5c959`  
		Last Modified: Wed, 01 May 2024 00:25:31 GMT  
		Size: 14.7 MB (14715897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c66e20fce587c50ce48922ecfd5690e8e78cb0420d78364f62ed62168dea31`  
		Last Modified: Wed, 01 May 2024 00:25:31 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e70b28fecd0d47f23539e1317d7465ba790af22b085ff0f326dbb2236a5fead`  
		Last Modified: Wed, 01 May 2024 00:25:30 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c5d08b65792340feca84531f54e216dd84fca1d6c3d502d289d6a33aede55`  
		Last Modified: Wed, 01 May 2024 00:25:32 GMT  
		Size: 52.3 MB (52319032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bd91b82ec81ce47c343e18ccb1978616891dc7a1ac33f9da16ace2a6ce7353`  
		Last Modified: Wed, 01 May 2024 00:25:31 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d173b5d2e02a7e7e0731459f3d77d9008b7d04cebbc4e382185c34ea54271f08`  
		Last Modified: Wed, 01 May 2024 00:25:32 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5500b6835297600dea208ecaba0afb60845d509752ba043c09e4dd2baf17d516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c710429c73bffafc957061a57a51cf15b9ffe1eaac3eb34963cdec2ad00716`

```dockerfile
```

-	Layers:
	-	`sha256:2ecfdf6b55b573267cec8c26eb177b2d4ea46a69674dd3596f0b96761460013c`  
		Last Modified: Wed, 01 May 2024 00:25:29 GMT  
		Size: 829.2 KB (829195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a346fdc98112d76aed07d5104bb1668239bb235d50176e9246d7fdcffd80092c`  
		Last Modified: Wed, 01 May 2024 00:25:29 GMT  
		Size: 36.3 KB (36333 bytes)  
		MIME: application/vnd.in-toto+json

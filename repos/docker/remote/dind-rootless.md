## `docker:dind-rootless`

```console
$ docker pull docker@sha256:699dd4ca65967fb818a76d6925a28b08f0ce41961fa1531d91b5b4cb1fe8e2c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:745bc27b41f4ed0a5110ca91af5f51bab24bed91eb7375dc27d5326c3fa5c9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153432661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cfcf9b1273ab1868ce76e3a19f4b678ea4f589f36bba4f844c21d2f7931f33`
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
# Tue, 30 Apr 2024 17:04:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 30 Apr 2024 17:04:38 GMT
USER rootless
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
	-	`sha256:862c2bedb703b28a4fc7f5e6d8259559c6e6bcf0491fb5b3427be60b603cb49a`  
		Last Modified: Tue, 30 Apr 2024 23:49:52 GMT  
		Size: 981.6 KB (981582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a447d5ff1cae9055d0078ae69f26e31c059f321daff993d83ce8c009ba87a32e`  
		Last Modified: Tue, 30 Apr 2024 23:49:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85bf80b428752a6bcf97cdaeb8e6999081db2be736f1a42feb295ce12cab3ad`  
		Last Modified: Tue, 30 Apr 2024 23:49:51 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b72d604609ae27346d01bd53cf7322be36a62e1da7cf4f5e23f07d867e688fa`  
		Last Modified: Tue, 30 Apr 2024 23:49:52 GMT  
		Size: 21.0 MB (20983891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17e0ecc2269a9e298c7648eef1ef300d837e4e64a2394d55940ab2a781f1ff3`  
		Last Modified: Tue, 30 Apr 2024 23:49:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e0990b2524427a8dda6bb037b3fd649d71561c28065a5f99cbdf365cb95998fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.0 KB (908965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540a7372fcc363b587d6c07f4a14ac029d895a8fa986b1bcbd05b4a41cfd47f5`

```dockerfile
```

-	Layers:
	-	`sha256:5ee5f3c3685a317dc7adba07a179984ca184ff1e842d7ca3ac4707aeb8756dc9`  
		Last Modified: Tue, 30 Apr 2024 23:49:51 GMT  
		Size: 875.7 KB (875706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edffd538cec2919e2c5444b95f863909595ea0d69c7a9338912eabd65df114f8`  
		Last Modified: Tue, 30 Apr 2024 23:49:51 GMT  
		Size: 33.3 KB (33259 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ea4e43890d5a1f86d1e544952d54c7b8ec8dc0122a302488371d0f06c5ed5a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146943203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3966d4642d12d1f225ad3516977839bd13c6304e159180a831fc941958e2a9`
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
# Tue, 30 Apr 2024 17:04:38 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 30 Apr 2024 17:04:38 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 30 Apr 2024 17:04:38 GMT
USER rootless
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
	-	`sha256:8d53702057bb4a77a066e443980ed232367433887bf22803f2928a58486f6ca3`  
		Last Modified: Wed, 01 May 2024 01:14:09 GMT  
		Size: 1.0 MB (1022615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594fc7d32a282afb6d3dd8812e66975fa32d9228b314886b9949750e923f37cb`  
		Last Modified: Wed, 01 May 2024 01:14:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb72999f58e4ae7ff7701ede517d7f4d33f761371cf7d44e7fea124d8f45f69`  
		Last Modified: Wed, 01 May 2024 01:14:08 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f447e4176abf274bd03d208680e7dc62e745403f09444b2b7d394414f88d659`  
		Last Modified: Wed, 01 May 2024 01:14:10 GMT  
		Size: 22.8 MB (22845786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee20e830c06a6f7bb2655937482f2147f0a2a91b557800c8ae3b9fcbee26349a`  
		Last Modified: Wed, 01 May 2024 01:14:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:15949b92c636aa33f7e263fc4a1626d19fd2f2fc7a8263de8cbe20f880931be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.0 KB (909040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6059202ad98af8a2b9ca0f82745acd5ff822ca9e06bb261718ec39cb1dd800cb`

```dockerfile
```

-	Layers:
	-	`sha256:2384ea747b49176b34fb7c19d41bb6432ae6102ac9b2c60a125db66efbe8ef83`  
		Last Modified: Wed, 01 May 2024 01:14:08 GMT  
		Size: 875.7 KB (875717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a707e14b610cb9cc48be8aaeca641c0d7c8258baf0ff208ac61c128d995ec83`  
		Last Modified: Wed, 01 May 2024 01:14:07 GMT  
		Size: 33.3 KB (33323 bytes)  
		MIME: application/vnd.in-toto+json

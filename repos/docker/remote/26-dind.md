## `docker:26-dind`

```console
$ docker pull docker@sha256:308c63f771a0596e23f6007f537c8e1d77c8cf68864f0a5a6fc476c69b9b7416
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
$ docker pull docker@sha256:5194addc8bc9afccee1a3ca04ddfe26b8c9ede2573e1823b33f5923395e6cc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131460188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53d90bb24113913e920d88247465f0196c54ea998a711e828260d9baf5de7ba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_VERSION=26.1.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 Apr 2024 21:49:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
CMD ["sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
VOLUME [/var/lib/docker]
# Mon, 22 Apr 2024 21:49:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612d43df1825367f3e7cc460359712d50edb80d67eca85b14fc4baaef3f3cc3`  
		Last Modified: Thu, 25 Apr 2024 18:52:12 GMT  
		Size: 2.0 MB (2026160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7104dac865754166d18a32ae6d1ced2a3bc9dc1ec76f1de5a54dafbd2e3de39`  
		Last Modified: Thu, 25 Apr 2024 18:52:12 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65d5c017567733fcb8fdf52038260d2884ff55eeb6ac010dd36e4f32359dcb6`  
		Last Modified: Thu, 25 Apr 2024 18:52:12 GMT  
		Size: 18.0 MB (18023048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ef7f86d9f84e411c695f63a8b8ec14f5b0aa348865fa77adc404a156e0f588`  
		Last Modified: Thu, 25 Apr 2024 18:52:12 GMT  
		Size: 18.1 MB (18078214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7cca4f6a3581c5f911f9bc9837add1296f07c6cec3707a7ccac031323d32c`  
		Last Modified: Thu, 25 Apr 2024 18:52:13 GMT  
		Size: 18.8 MB (18764669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd619a5b8413dfe87c9aafc5a7adc67aa3e18d4d447732ebae72f71859f9c9cc`  
		Last Modified: Thu, 25 Apr 2024 18:52:13 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556c27015097c8fd89beda2486392ddf5c0db1c48c81a203bba6ef3893d677c4`  
		Last Modified: Thu, 25 Apr 2024 18:52:13 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedc2ef270f1a9ac503de7af81b62da42bee0dcf5ddfd8ef7845e4e43585b2`  
		Last Modified: Thu, 25 Apr 2024 18:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771aa884b5c147e304b22b94846e9e470b20034e4c48dc49a6903e2e76a37853`  
		Last Modified: Thu, 25 Apr 2024 19:52:30 GMT  
		Size: 14.4 MB (14355021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b358e5f624f15a6cddfdc992390c0d3cda313e58a98b0e872f8ba09854dee3a6`  
		Last Modified: Thu, 25 Apr 2024 19:52:29 GMT  
		Size: 89.1 KB (89141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e395d0208700430f1ece7abc970cd0f59329014126b243450638be942e2a0c2f`  
		Last Modified: Thu, 25 Apr 2024 19:52:29 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce88d90e9904f5a7396da894d1589db40dee39a928f4c38b00e4c9a8b960002`  
		Last Modified: Thu, 25 Apr 2024 19:52:30 GMT  
		Size: 56.7 MB (56706883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde67919e45d3a85a7f1a3837639586b078733e5ec954262307769a9487da34c`  
		Last Modified: Thu, 25 Apr 2024 19:52:30 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffed0f3d0f3a01577410760ff71ada7d76306a7b110bbffb45a403ee3f15e040`  
		Last Modified: Thu, 25 Apr 2024 19:52:30 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f0275be533e25e551fbf0f8553c7c2ca7b1f70eb53061de5c380df98285b4921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.2 KB (864175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4917c6060365a3153b15b109a38619e37ae061277cf4a0169f03d138e8e0f8a`

```dockerfile
```

-	Layers:
	-	`sha256:d511dea96acc715fd10a41a4875418a8f654035ceb51c4716b47f062a0e57bd5`  
		Last Modified: Thu, 25 Apr 2024 19:52:30 GMT  
		Size: 827.9 KB (827918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f5bc7cd4a515fffb8b259a5c7f321c8f0f715549a6bfad916effe9cbfbb07b4`  
		Last Modified: Thu, 25 Apr 2024 19:52:29 GMT  
		Size: 36.3 KB (36257 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:95fae91dc5e0cf4e4778d06a60bb88c2c16a57f7328b4a963abee82aa987d17a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123643008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fc2a352f1f1246ad70be74cedc311d6d3b4bac89c554e791a5c8d5202aedc0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_VERSION=26.1.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 Apr 2024 21:49:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
CMD ["sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
VOLUME [/var/lib/docker]
# Mon, 22 Apr 2024 21:49:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
CMD []
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df81b92ba1f4156d8bc09cde32c3c3acb72b2f836feed84f459a8fea520b95f9`  
		Last Modified: Thu, 25 Apr 2024 18:55:41 GMT  
		Size: 2.1 MB (2116804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcda65bc8fc7021d053af60b2ed4275e6fb0af9165da9aad60f3294b016a4d2`  
		Last Modified: Thu, 25 Apr 2024 18:55:41 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bd24dfe95650bc354d06643eb02e6d779571adcdf54ff7fe96f3ff0262fba3`  
		Last Modified: Thu, 25 Apr 2024 18:55:42 GMT  
		Size: 16.3 MB (16316781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c932ef28687bcc82b56ea1b136711536afe74073bd93bbeba9c3567d577d15a4`  
		Last Modified: Thu, 25 Apr 2024 18:55:42 GMT  
		Size: 16.9 MB (16915891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8979c2c753423e4a40d511b21c9a535c4ca6b91e39c8d47f2b65271029be1`  
		Last Modified: Thu, 25 Apr 2024 18:55:43 GMT  
		Size: 17.7 MB (17726572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc07250aa40bb6a3a5370a9321803e53cdd78849ed024d08b4d17ac2e479feb`  
		Last Modified: Thu, 25 Apr 2024 18:55:43 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de602837a1d71055545866ad31ae41bed499aeb9ce2453a2ab915f74de22ef59`  
		Last Modified: Thu, 25 Apr 2024 18:55:43 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a5720df65ec9f5dad918a43e510e9775ab71e2d27e0a24670296d053b66f11`  
		Last Modified: Thu, 25 Apr 2024 18:55:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219de67b1126a13a4bc3ddbf3168a5e79e11ccf17374494325c915b50d0366cf`  
		Last Modified: Thu, 25 Apr 2024 19:56:45 GMT  
		Size: 14.3 MB (14316682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f081172d7c5b9810d4b4c13fcc2f31730af916a37a2fb151ceb4bbb83237a2c`  
		Last Modified: Thu, 25 Apr 2024 19:56:45 GMT  
		Size: 88.4 KB (88362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555041be6800b9099a1fb086285fc1a97251614bddd127c90cc4301145b34395`  
		Last Modified: Thu, 25 Apr 2024 19:56:45 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddddfa426816422be758d0839e7bfae9ceee1bbd8f3d5706349224eee954ddcd`  
		Last Modified: Thu, 25 Apr 2024 19:56:47 GMT  
		Size: 53.0 MB (52988198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4060fb9a887e7bb0309586ac3057867b2e6d0ce0d2e226c7ad66b081f3461eef`  
		Last Modified: Thu, 25 Apr 2024 19:56:46 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841a52e686bfae7d7fb092d5305c0e2836d7881cbab67fd14b51989493d0f072`  
		Last Modified: Thu, 25 Apr 2024 19:56:46 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0bbbf9a354db269f888fb1524da4fa835f2b46f9f067e59366224f0c39d07c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 KB (36261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4666ba072ce8e99a13b628fb2ac76a6ae33daae00d113c61a9189814e37c0ab`

```dockerfile
```

-	Layers:
	-	`sha256:46a67d8e5ba65b93d392853a310dd081bfa5d38e4f5901f4eb8253ad6ee05d37`  
		Last Modified: Thu, 25 Apr 2024 19:56:44 GMT  
		Size: 36.3 KB (36261 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f44aee367c2641abfba94759bbb79ae208d50634129aada95d479af67c3d76e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121847026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc19779b2a34d2e1e2026cd17e360ce47916bbe35e60ca4a535bf9b0599acccd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_VERSION=26.1.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64'; 			sha256='f3ba3bf1e4ab18e96c2d36526a075a02a78fb5f8e80d3e3ca9c5bf256d81d0a0'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv6'; 			sha256='ee467093d138f9c4d189b774552ef86ba253107bd91226b28f0c54edf62fe949'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-armv7'; 			sha256='8461b4d4a58eaaf04c4f482f0dabe57db9ef63229311a9583c6548b417f33c76'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-aarch64'; 			sha256='37a1c197fef5fda2a3df2d5ae0d7762ad2a00e30946ad06d4ad9fa8cef16d9e7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-ppc64le'; 			sha256='faed2dd8f0568922dadf1a8fa155898d5be1feaa67568f2aa730a594ba6a44ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-riscv64'; 			sha256='71a09bd1980505a5f194cfab5df53bba55e493edf246f3ebb28cbfef8caf7715'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-s390x'; 			sha256='d38522261b481d7f20da7f80af67824afe2a1b54dd19215690febb0c49ad932d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 Apr 2024 21:49:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
CMD ["sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
VOLUME [/var/lib/docker]
# Mon, 22 Apr 2024 21:49:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
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
	-	`sha256:5b997f4a09b13721711ce7c71b8f509e7b0019d149ff8cc16ffddf8e42df2f17`  
		Last Modified: Wed, 24 Apr 2024 00:23:28 GMT  
		Size: 16.3 MB (16309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a27cacf881615cf414b1487293c399bd22894746376e675dd833046a298851`  
		Last Modified: Wed, 24 Apr 2024 00:23:28 GMT  
		Size: 16.9 MB (16901909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efd175250621532632e98c4b812471d1016341f3f5fd5a069bbad4d7a268ee5`  
		Last Modified: Thu, 25 Apr 2024 19:05:15 GMT  
		Size: 17.7 MB (17710688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065c7c6c39542590fb238bd5e5b65ef71428c277536c22ff77747059e95ca511`  
		Last Modified: Thu, 25 Apr 2024 19:05:14 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9595d85cdf1718473c35a3caf8c8a862b0c599076b193b9860182b3eb66c9e61`  
		Last Modified: Thu, 25 Apr 2024 19:05:14 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6708b32f17b3dab048216769e865060dde6131fee29335f04dbd0d0d93c5b00`  
		Last Modified: Thu, 25 Apr 2024 19:05:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f23d8e525de53b05a2f9e30e18319fdf0cf5fc1035b8837d61f747ab56827b`  
		Last Modified: Thu, 25 Apr 2024 20:06:32 GMT  
		Size: 13.0 MB (13029193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd74ad45ebb39801169e5d9114d99ffb0d2a4801c57087118958fe42c7448a7`  
		Last Modified: Thu, 25 Apr 2024 20:06:32 GMT  
		Size: 84.3 KB (84283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba8f5a1ed45a84b1dc021242373b337df2a72b9819be56d6438e60bf9e397b`  
		Last Modified: Thu, 25 Apr 2024 20:06:31 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4099ac98c64e39ddb109fbc0ab3cd75a2dc6172e6bda0157b35c99aa35879eb8`  
		Last Modified: Thu, 25 Apr 2024 20:06:33 GMT  
		Size: 53.0 MB (52988313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6160a5dd468cb9e30002de09fd2810f9f9a8676dc01f37afc0335d10b10fcf04`  
		Last Modified: Thu, 25 Apr 2024 20:06:32 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b3d64b491c312b01a6fe9a5bf978c4e8f6c0f1dbaf160f03651263c6fee49d`  
		Last Modified: Thu, 25 Apr 2024 20:06:33 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2074c3de521437acfbda697e5f28d8874b7d773ec5677f1731697eddf48a0ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **861.2 KB (861166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e22d50b7dbbd0729e04ec6d454d965c9e33e4e51240fe8848996d3ee04baa5`

```dockerfile
```

-	Layers:
	-	`sha256:7669dd6625dbb1bdb126d4b3c015a8d2a83cadaaf4e807b3fd04fcd79e798269`  
		Last Modified: Thu, 25 Apr 2024 20:06:31 GMT  
		Size: 824.7 KB (824685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:387b0c1af5b2af3b5c2961f568b8af646347445c4ec78f3fbb39c15faeb21e96`  
		Last Modified: Thu, 25 Apr 2024 20:06:31 GMT  
		Size: 36.5 KB (36481 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f85cfae029f2f0fe39a366fa35ebeb6d16eba3faf3f898dd5ed3520460bdaec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122968654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8b8bc56476031277861c515fcc9ecded6e24550efe7667c4c442a5f95f52e9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_VERSION=26.1.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 Apr 2024 21:49:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
CMD ["sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 22 Apr 2024 21:49:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 21:49:05 GMT
VOLUME [/var/lib/docker]
# Mon, 22 Apr 2024 21:49:05 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 22 Apr 2024 21:49:05 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 22 Apr 2024 21:49:05 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b275a3377f65492f727dc46aa2b70be6ec8ff96583fcd9a7b699692b5170bc`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 2.0 MB (2019704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c53acdebd8fb391eae546ed72149f049f8ab4d594f12c74c49be04cc3b9708`  
		Last Modified: Sat, 16 Mar 2024 04:06:08 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6cb7f8dcca06497c57484ff8eb9a5fa47eff1d2b450ea5e313808885d75d49f`  
		Last Modified: Wed, 24 Apr 2024 01:34:07 GMT  
		Size: 17.0 MB (16979682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0074d7eb4eefb10d90fef4e52563f5003cc933e5eaeb53fe23c881daa9e021`  
		Last Modified: Wed, 24 Apr 2024 01:34:07 GMT  
		Size: 16.4 MB (16441655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9c6299c0882bcc84d03062288bf0cd7fb74a4b3dd4f1d6ff6ecd354966da1f`  
		Last Modified: Wed, 24 Apr 2024 01:34:08 GMT  
		Size: 17.0 MB (17047136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb177eab0b0431234b61ab934a94791cbecbd5b6e44591ede4c466946d0e737`  
		Last Modified: Wed, 24 Apr 2024 01:34:07 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22085cf3c8676c6a0eba65f96551c7f35e9b9149a85f6b07b4a1ccc99e6b271`  
		Last Modified: Wed, 24 Apr 2024 01:34:08 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f10a6ec2c2b7aa8439911a911d901949a6d1a94c18e2aaed2ea91c3543eb23e`  
		Last Modified: Wed, 24 Apr 2024 01:34:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf8ff61bc5a8025cd17727ec33b464b733f2dae1b63b15ee115d74c2ff2512f`  
		Last Modified: Wed, 24 Apr 2024 02:29:08 GMT  
		Size: 14.7 MB (14710061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9303f0ee38a19fdf1e1f10282d4aec4b736c2e8fc92108fb393919c35d0a82`  
		Last Modified: Wed, 24 Apr 2024 02:29:08 GMT  
		Size: 98.4 KB (98394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08e06eb9c4d0089a261b456671e3f0d2bb0de87a895e837120353adcd928700`  
		Last Modified: Wed, 24 Apr 2024 02:29:07 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a261482e36a8ade4c39ee9dde2b8d232b8c75f500644754d9c52e7a30a0dd334`  
		Last Modified: Wed, 24 Apr 2024 02:29:10 GMT  
		Size: 52.3 MB (52315981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d297f16aa8980c8d0d53b2889488da0728ee97c283b9e2595ab62fc9c2dd287`  
		Last Modified: Wed, 24 Apr 2024 02:29:09 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9901e32679cc2cf8330a70a7abfa4b13152ee2349a634dd5ed6be0d178d2a1a5`  
		Last Modified: Wed, 24 Apr 2024 02:29:09 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind` - unknown; unknown

```console
$ docker pull docker@sha256:443e6cd6f9f22ca2e686bc6f8ca6b1318bfca1dade3b74004eeb45ecd6ffd88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **860.8 KB (860768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29539f3a96cd15d711825c839f6288aefa780460dd3a2bf1eef61c8e15773633`

```dockerfile
```

-	Layers:
	-	`sha256:c4e6753cbe441863f5405bbec44334e10257f8629cba7c638db9db4c51557009`  
		Last Modified: Wed, 24 Apr 2024 02:29:07 GMT  
		Size: 824.4 KB (824435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3bd9f2199351a47fef72083daddbf1406b6b787f8cafa151c5b7ce0dfb7dad`  
		Last Modified: Wed, 24 Apr 2024 02:29:07 GMT  
		Size: 36.3 KB (36333 bytes)  
		MIME: application/vnd.in-toto+json

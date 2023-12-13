## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:63d2e1468b562c0f815b95c3af7596ac86989d0810df3fb594de87bda08e0c61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:bef31397a5a3b53ae97a9e5b097e96645b9b73197fdd7e0c6e7d9578929afc21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142207933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b26d86cd7fe457e3994ddd1cd389cfaf69a4950dc5007e21feb3e1b5c14be03`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Tue, 12 Dec 2023 23:39:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENV DOCKER_VERSION=25.0.0-beta.2
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 12 Dec 2023 23:39:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 23:39:18 GMT
CMD ["sh"]
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
VOLUME [/var/lib/docker]
# Tue, 12 Dec 2023 23:39:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 12 Dec 2023 23:39:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 12 Dec 2023 23:39:18 GMT
CMD []
# Tue, 12 Dec 2023 23:39:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-25.0.0-beta.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-25.0.0-beta.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 12 Dec 2023 23:39:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4823d20c120d2f1658d164f8c3016c28be9f959c31c06e2eb4ec6b905cfadd`  
		Last Modified: Wed, 13 Dec 2023 00:49:34 GMT  
		Size: 2.0 MB (2014288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d4655980096e41fcca4075f7fe147a46c1c10443025a8ec42e332ce86287dc`  
		Last Modified: Wed, 13 Dec 2023 00:49:34 GMT  
		Size: 16.9 MB (16879767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c931e8eff7bb3364ff95035fc559bf6678ae699de14f17d74dcf38206d725`  
		Last Modified: Wed, 13 Dec 2023 00:49:34 GMT  
		Size: 17.2 MB (17195293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e59ec295362a40622809fba9dbc565160c0f91116457b780e50ad1d42ba635`  
		Last Modified: Wed, 13 Dec 2023 00:49:34 GMT  
		Size: 17.9 MB (17852058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228b86ec12aa959c023bcca94ed2eb2c98fa0af43c156a2ecade80b5087d28d2`  
		Last Modified: Wed, 13 Dec 2023 00:49:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c422a5b024ba2956bda95aec4209a81e245713f69a957e6e5625ab5dd586cd4`  
		Last Modified: Wed, 13 Dec 2023 00:49:35 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f74daa819276a44f3bbc4d5089ae4b8dc7c6c3d9ea90a00b9a5abef46a162f`  
		Last Modified: Wed, 13 Dec 2023 00:49:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9048934c24150c9e949c53488dc76694470138c6c4bb64efd7d141e593953`  
		Last Modified: Wed, 13 Dec 2023 05:51:44 GMT  
		Size: 7.1 MB (7083724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f945677c9a07aba8e452a1cecbb50b81af589336524240fed6a957e97f274aa8`  
		Last Modified: Wed, 13 Dec 2023 05:51:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fc571bd11696b7a227216e3010c95f3a6ccc7228775926342645e596411fa7`  
		Last Modified: Wed, 13 Dec 2023 05:51:46 GMT  
		Size: 55.5 MB (55546293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7548fa5e4e5f56690126d1549f4ec592bec8a420f9e3e60addee7180806af9e`  
		Last Modified: Wed, 13 Dec 2023 05:51:45 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17542bb52f411ade84fc5b02d5b6048ab9dab867b9ee9e8880281303d02c95f`  
		Last Modified: Wed, 13 Dec 2023 05:51:45 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52a9b59feb0add74f95254ade03792cd5dbd938b8b180221c21f314afed7101`  
		Last Modified: Wed, 13 Dec 2023 09:49:51 GMT  
		Size: 1.4 MB (1362324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afaa1fffb081c28eebcab47097bf4db47a42c837255fa24f2b072f351e4eb4d`  
		Last Modified: Wed, 13 Dec 2023 09:49:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1d530e027b378fb92171c60725bd831e02c20e348a0beca49161bb785f298a`  
		Last Modified: Wed, 13 Dec 2023 09:49:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fb313a44bfa5d6723a7407150c62677aebf583f4cafbf20f9e2b2566e341b0`  
		Last Modified: Wed, 13 Dec 2023 09:49:52 GMT  
		Size: 20.9 MB (20862829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22df0fe70938deccca5ac2af94071bd1ecc639b8debdbd200973551d74391181`  
		Last Modified: Wed, 13 Dec 2023 09:49:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b1859d31a18a6ec4f6ae29d8e9f4a3fec3784b86cb76d25c3771c697f8c23d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.4 KB (756387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c56c7912f11fdf83bc46e24d96f9b6a2df1fdadddd8bd1abb66c6cbe1312c`

```dockerfile
```

-	Layers:
	-	`sha256:a64cdab6edc209c828cf6ebb8aa74f42cf0c882619815ee4f6c4db5d81eee71a`  
		Last Modified: Wed, 13 Dec 2023 09:49:51 GMT  
		Size: 725.5 KB (725530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bcc3225bc54d75254c24b613212b6e03588d76cfa65b964a542ff1b8a939eec`  
		Last Modified: Wed, 13 Dec 2023 09:49:51 GMT  
		Size: 30.9 KB (30857 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bfbcfecc9968b89f2ffd0f23140992da1b8d6022194aa69d336d7da28c4e34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135896038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b7681766ed23fe8adc4320cbeba94ac059a6a02e79e05a7a8d49a1ef5dd9b1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Tue, 12 Dec 2023 23:39:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENV DOCKER_VERSION=25.0.0-beta.2
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 12 Dec 2023 23:39:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Dec 2023 23:39:18 GMT
CMD ["sh"]
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
VOLUME [/var/lib/docker]
# Tue, 12 Dec 2023 23:39:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 12 Dec 2023 23:39:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 12 Dec 2023 23:39:18 GMT
CMD []
# Tue, 12 Dec 2023 23:39:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-25.0.0-beta.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-25.0.0-beta.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 12 Dec 2023 23:39:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 12 Dec 2023 23:39:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f34bfa1504ce7e2d8b894097d2570cc4740496235ea69363a5ef829254cad47`  
		Last Modified: Wed, 13 Dec 2023 04:34:56 GMT  
		Size: 2.0 MB (2024568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6213e2c2584e4cbd8b741f968870167ba92510384b985fb3aeeafb8aed08e10`  
		Last Modified: Wed, 13 Dec 2023 04:34:57 GMT  
		Size: 15.9 MB (15895326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f5a77cd34a9a119ff31f008ac5f33580a3332d54304e9af198bff951887a2c`  
		Last Modified: Wed, 13 Dec 2023 04:34:57 GMT  
		Size: 15.6 MB (15640596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4372cf38b09aafc5d302d28ce48e06b404cf13e1a4954280e947186baaf77e`  
		Last Modified: Wed, 13 Dec 2023 04:34:57 GMT  
		Size: 16.3 MB (16302309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d0cdbe692c8bc7ae869b6b3ec0d5e3972c88907521b7af489e5df4aecbea84`  
		Last Modified: Wed, 13 Dec 2023 04:34:58 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2e36855e856e93adc63c7daadf1b813f2672d2283c55be1f405afd4d380209`  
		Last Modified: Wed, 13 Dec 2023 04:34:58 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4aa3933a7691c8f9a319802cdd4d05304af4e0b823629e0cd8f5e1da8076e7`  
		Last Modified: Wed, 13 Dec 2023 04:34:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49a3fc6c7c842633af7745967f76bad0b2fe5538bf0c84e53620216fd882ab7`  
		Last Modified: Wed, 13 Dec 2023 06:13:01 GMT  
		Size: 7.3 MB (7293922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bb4c62f054f25e5c110e04b8324bc3833737d9cf7d8479f31a0c94b8ce3075`  
		Last Modified: Wed, 13 Dec 2023 06:13:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2904ee00fe498cabd7774c6f0b8306a7ddccb92c2f9845c882b849059ef679e8`  
		Last Modified: Wed, 13 Dec 2023 06:13:02 GMT  
		Size: 51.3 MB (51254980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ee851f06d53aea1e13295be5dc3510f35f8fa500053bc50c4ab478890491f6`  
		Last Modified: Wed, 13 Dec 2023 06:13:01 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fba8893e4970009bee83019210b024505cff4667a3a42c146bc6d2e0eff8da`  
		Last Modified: Wed, 13 Dec 2023 06:13:01 GMT  
		Size: 2.8 KB (2788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6047a714db29f782aaa50555600b3f53d9fd6fb45d77451372e15d6acc531005`  
		Last Modified: Wed, 13 Dec 2023 10:01:06 GMT  
		Size: 1.4 MB (1413217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83629b7598ee8ce529aaf616d3a5d212d7ca398217df2f3e52ab87f4f228f7a`  
		Last Modified: Wed, 13 Dec 2023 10:01:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ef3cce6a18fa6b8002f7e3a469d8606f561f018c57753645fa4bb678309806`  
		Last Modified: Wed, 13 Dec 2023 10:01:06 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c61d0980cf17399e24ff8637498feefc006ce394efd46541e26fdf19037d7`  
		Last Modified: Wed, 13 Dec 2023 10:01:07 GMT  
		Size: 22.7 MB (22729161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7290aef6afdc7da42d16c8ac394108de7b87584d5ac63c74b62cb86b18ba2d`  
		Last Modified: Wed, 13 Dec 2023 10:01:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:85077e8849c64b37a6494f733013175d3059c1b052a155e19aac6c2da820a240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.5 KB (756453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa59d45d0dd5e9e59c7c24b6dcf69407582dbb9a659f3fbbbc5cf065bba4a233`

```dockerfile
```

-	Layers:
	-	`sha256:a4de5451ffd6b8b096bc310be1c08d215144a9805fcc7fdcd960301ac2a8b9a8`  
		Last Modified: Wed, 13 Dec 2023 10:01:05 GMT  
		Size: 725.5 KB (725539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a5f58e7a9ac0549f739f64f7e54206d75e3187bcadcf32e0599cdef90664f15`  
		Last Modified: Wed, 13 Dec 2023 10:01:05 GMT  
		Size: 30.9 KB (30914 bytes)  
		MIME: application/vnd.in-toto+json

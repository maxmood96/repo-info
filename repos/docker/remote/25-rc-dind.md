## `docker:25-rc-dind`

```console
$ docker pull docker@sha256:2fdfc246e397f7eea0081aea60898e727d4b515131ba987af5d539bec3594d61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:25-rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:0a71a25e703d5ec1c5a9460aa0bc80cac80910eb08d5abab3db5fb4490091ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120206571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2ad49e09ef35a149880da6440cd300cf863849a2725b20f507ceec7a4ad5df`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 23 Nov 2023 12:05:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 23 Nov 2023 12:05:52 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:05:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_VERSION=25.0.0-beta.1
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:05:52 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:05:52 GMT
CMD ["sh"]
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
VOLUME [/var/lib/docker]
# Tue, 28 Nov 2023 00:06:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 28 Nov 2023 00:06:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 28 Nov 2023 00:06:31 GMT
CMD []
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e800fcde722b6440bc910e7cd975dc683bec9ee486590ebee2c15ada7261452`  
		Last Modified: Fri, 01 Dec 2023 00:10:40 GMT  
		Size: 2.0 MB (2014295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53a0bc94727cf3076969b24cde06063b6603ae043bc8f44c23dcfcc384bdf6f`  
		Last Modified: Fri, 01 Dec 2023 00:10:41 GMT  
		Size: 16.9 MB (16890677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d261604f5b65b71c18d4906e03861275886fa334cdc75c1134669e5f40e83ccc`  
		Last Modified: Fri, 01 Dec 2023 00:10:41 GMT  
		Size: 17.2 MB (17195306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410eab12c67f92700680ce08f86bb1bafb64e15fc2a6e835c7cb0fa64ced24eb`  
		Last Modified: Fri, 01 Dec 2023 00:10:42 GMT  
		Size: 17.9 MB (17852071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4651667180a0b553f2615f5fc7f2dc842b66fbf7231540b2260f001c16ec900`  
		Last Modified: Fri, 01 Dec 2023 00:10:42 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ca2f2dd8b9a70c7f4bf82664d7c9990b67f477c19c0579eb686105cf77d7ac`  
		Last Modified: Fri, 01 Dec 2023 00:10:42 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c8b600ba6a8f4ba832451905f95a54ee8118edf51c36c620e7710d1793a692`  
		Last Modified: Fri, 01 Dec 2023 00:10:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f84f7a0e37d68bb62b261ecdccf6570204544f344f75322d49bf58f8ecc527`  
		Last Modified: Fri, 01 Dec 2023 01:11:41 GMT  
		Size: 7.1 MB (7080282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4336b09548e5a3005eeea67d1c894fdc0d914d1e4a025f15df03bc73084eb83c`  
		Last Modified: Fri, 01 Dec 2023 01:11:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f25b6b4d196222d89ce173712d36cfe2ed5d6355626125bba3031ee91dc13f`  
		Last Modified: Fri, 01 Dec 2023 01:11:41 GMT  
		Size: 55.8 MB (55764212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebb483dccef6eba6c3901a1bd5bc7659339ae0ab9218a270e8821d1ce4141c1`  
		Last Modified: Fri, 01 Dec 2023 01:11:41 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a86d4161a926e166bfcb3e5d8011152d266fe09e9df6875c255676db951a81`  
		Last Modified: Fri, 01 Dec 2023 01:11:41 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3153567efaee5709b682580b676113d3c1c1e7b3dc6dc60c05e9e869bb25f035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.2 KB (702183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1ff768018c093383ff277f8e739bd152f79868a226f86bd332322ed6a41db7`

```dockerfile
```

-	Layers:
	-	`sha256:edec46424fbf13dd3184bc11859b729b3bfd2d1d7f7017a58986fd3f04b31f2f`  
		Last Modified: Fri, 01 Dec 2023 01:11:41 GMT  
		Size: 672.5 KB (672495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8862e466ead584c432caa549724f4a49737999e979551fcaa2c10fcb2d1b65fb`  
		Last Modified: Fri, 01 Dec 2023 01:11:41 GMT  
		Size: 29.7 KB (29688 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:9c7fa61ea10cd099251fc9f02a8f5f8e4a64fdf2d88978ccbdbbbffb2a89feb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112772098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9891d78b3a6e8552056e80dc3112baafd74b33d0641e6419f90a3d6d63a88390`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 23 Nov 2023 12:05:52 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 23 Nov 2023 12:05:52 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:05:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_VERSION=25.0.0-beta.1
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:05:52 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:05:52 GMT
CMD ["sh"]
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
VOLUME [/var/lib/docker]
# Tue, 28 Nov 2023 00:06:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 28 Nov 2023 00:06:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 28 Nov 2023 00:06:31 GMT
CMD []
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcbe62a68d12d326a6216794589666f3880a1b7f916f47a323045227af69af0`  
		Last Modified: Fri, 01 Dec 2023 11:44:39 GMT  
		Size: 2.1 MB (2088618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22f22222458c3464e3fed01d85502fca59d061f28d43b44dc015e398d3010dc`  
		Last Modified: Fri, 01 Dec 2023 11:44:40 GMT  
		Size: 15.3 MB (15274898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4164564bff0273ff1d1e1e81f936c90002cbdef8ff8e962c977f6d84255152db`  
		Last Modified: Fri, 01 Dec 2023 11:44:40 GMT  
		Size: 16.1 MB (16099973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b2941e4b3a7cad42f442fa390f6bd274f4eb2040e326c5c7ce9c0308e0959f`  
		Last Modified: Fri, 01 Dec 2023 11:44:40 GMT  
		Size: 16.9 MB (16867511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cb1847d6aa40d93b86a95c398d59657c2583f82d7ca86a5cf7c41826c066ad`  
		Last Modified: Fri, 01 Dec 2023 11:44:36 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9094ed30fbdd2c34b8df7597a59fa4336d3e87d4a26502d4313988e2bccf327b`  
		Last Modified: Fri, 01 Dec 2023 11:44:36 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a758b1f233735cd8e6aa0f4008ed4da3278d786ea8a475b56f836b949d22963`  
		Last Modified: Fri, 01 Dec 2023 11:44:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87676a1d45001c44981a8e46ede1005fc3c23420cfa0c9e47467f735007224dd`  
		Last Modified: Fri, 01 Dec 2023 13:24:58 GMT  
		Size: 7.2 MB (7173663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e4f9e5daac1156eac0d1ed3bb110d4fd2d26a1cb285c59921fab3b93849bfb`  
		Last Modified: Fri, 01 Dec 2023 13:24:56 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c712ea6c171dc8de34091def571838949646c05ef5986f9a6163f2a7ea7dec`  
		Last Modified: Fri, 01 Dec 2023 13:25:05 GMT  
		Size: 52.1 MB (52113247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30a89b8b9ff812c53eee159d884698d309be1b1fbc61314263fe5dfeb8ce450`  
		Last Modified: Fri, 01 Dec 2023 13:24:56 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12e9dbba87a0f85dfe162aba9be0fded44e17934e24fd7dac4168e0ca4ea613`  
		Last Modified: Fri, 01 Dec 2023 13:24:56 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:25-rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:2c0a6d2b990973c29a9715071cf36cf82c4362812a54fa306bdc4e85c4b38fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111573260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1338b301e7fbdeed4c28b2ff9dfd15af2d0ec6ea6ec25d7234111dba3ae90b62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 23 Nov 2023 12:05:52 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 23 Nov 2023 12:05:52 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:05:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_VERSION=25.0.0-beta.1
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:05:52 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:05:52 GMT
CMD ["sh"]
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
VOLUME [/var/lib/docker]
# Tue, 28 Nov 2023 00:06:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 28 Nov 2023 00:06:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 28 Nov 2023 00:06:31 GMT
CMD []
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95efc36d5bd6e6f6cacfcd0475b060ca3cf0b73388d577a29cf0e1260082d17`  
		Last Modified: Fri, 01 Dec 2023 10:04:32 GMT  
		Size: 1.9 MB (1875249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64eb4c226d2ca8f721d5c290cdccebfd2ef6288e8f7131c18d985890c9ca109d`  
		Last Modified: Fri, 01 Dec 2023 10:04:33 GMT  
		Size: 15.3 MB (15269612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d7ea31035368e81084d65946b1d719343b1df42728324f704de10e40885fd3`  
		Last Modified: Fri, 01 Dec 2023 10:04:33 GMT  
		Size: 16.1 MB (16084090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edafbacaf153673c1cb5b9e47c9377ca33178b1c99363b6470c0cc9f1c126f7c`  
		Last Modified: Fri, 01 Dec 2023 10:04:34 GMT  
		Size: 16.9 MB (16852961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24261082fd8d37f0a7b3f6d7a6aedeae1f4b27af42b163951aee449d7a9c6d80`  
		Last Modified: Fri, 01 Dec 2023 10:04:33 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7424a667b3c987af54b2c9762d8566ceb51717fd91308a6b8e2ff3f0e732e1f1`  
		Last Modified: Fri, 01 Dec 2023 10:04:34 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fd3dfab6efc6681b2f2c0ab579edf4699a222ab2f7caf927b15aba68dceff0`  
		Last Modified: Fri, 01 Dec 2023 10:04:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f9a84de65e35972264729cf7b3ffe4dc19d0fcadcda5f5c2a5eae0fdbee631`  
		Last Modified: Fri, 01 Dec 2023 11:56:54 GMT  
		Size: 6.5 MB (6469751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d71badbc4d0b89d41805f7dcd13041981854e9f9224b6eabf9e4cc5ac48709b`  
		Last Modified: Fri, 01 Dec 2023 11:56:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beadc5727012fa1705be252ab7dfb493c1153c4148da063ebe60a537c7e140d4`  
		Last Modified: Fri, 01 Dec 2023 11:56:57 GMT  
		Size: 52.1 MB (52113283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0d6342d723b65124ec6c2d8998c95444fc4f2254a295b6048b98a3387606a4`  
		Last Modified: Fri, 01 Dec 2023 11:56:54 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35bade4422c3b5a5ace89ce856adf000a37491b0908e341b76066090861183`  
		Last Modified: Fri, 01 Dec 2023 11:56:55 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:15fbd73c9313b4af7cf649227881a6c10310ddc09baa871727321cbc85133f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.4 KB (702440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c7ee7df5886e693edf7f29a2d1f443d8bab4fcbda292ddd7817978dcfd640f`

```dockerfile
```

-	Layers:
	-	`sha256:ba78f43536e5c506fda411fc9e644840dc9f0c11823de45d8993d2aacb8ab72c`  
		Last Modified: Fri, 01 Dec 2023 11:56:53 GMT  
		Size: 672.6 KB (672563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70af1a1af0fc49c12fba9acf1357812c1a0aecbda02bf6ec1874d0f7db4c1067`  
		Last Modified: Fri, 01 Dec 2023 11:56:53 GMT  
		Size: 29.9 KB (29877 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:009176f4705289425d856f4b8ea7191cd252d51c5eacb748754e58702f174555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111881271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b769d20ce43441b929102c2de47450657dc842f07592adaf2ceb94791299f889`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 23 Nov 2023 12:05:52 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 23 Nov 2023 12:05:52 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:05:52 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_VERSION=25.0.0-beta.1
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:05:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:05:52 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:05:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:05:52 GMT
CMD ["sh"]
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 28 Nov 2023 00:06:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Nov 2023 00:06:31 GMT
VOLUME [/var/lib/docker]
# Tue, 28 Nov 2023 00:06:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 28 Nov 2023 00:06:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 28 Nov 2023 00:06:31 GMT
CMD []
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26858e57ca6ca6c73ea7609b8f22c6a8f69a2e37b3e4147e8b5e125aeb518205`  
		Last Modified: Fri, 01 Dec 2023 11:42:31 GMT  
		Size: 2.0 MB (2024551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384180d09aea44462fb423a4021068a3f446a931925cd366fad476ffa2bcfefe`  
		Last Modified: Fri, 01 Dec 2023 11:42:32 GMT  
		Size: 15.9 MB (15893487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4827e5cd4f81d47eb4dbd0799e67948615352bc480463ef7a2d4687a2d27aa4`  
		Last Modified: Fri, 01 Dec 2023 11:42:32 GMT  
		Size: 15.6 MB (15640608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ac403a66fbaa550bf4064ec1253f4fd8eb679ced15be7b6ff7be9d334c75b3`  
		Last Modified: Fri, 01 Dec 2023 11:42:33 GMT  
		Size: 16.3 MB (16302308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05eb3967a63d61b71ae71f139fc1f409709545dda50899e278ae8d25a35dca3`  
		Last Modified: Fri, 01 Dec 2023 11:42:32 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aa9b80b76fd67c3e67dc6cb741daa3cb9eb9566843cf01ff8c6b428c0c462d`  
		Last Modified: Fri, 01 Dec 2023 11:42:33 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b43aa86ed57146c4ee2b964a46fc067c330fb671d37d56bf384cb5dcfc85e5`  
		Last Modified: Fri, 01 Dec 2023 11:42:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6d8c506ebac2e26252859576f1779c91dbc042f229fa57015073caf26135f7`  
		Last Modified: Fri, 01 Dec 2023 14:31:21 GMT  
		Size: 7.3 MB (7291389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a32b541a2d0beab8e26965f345fa8de74c125d6222fe94f2a62840b3446046`  
		Last Modified: Fri, 01 Dec 2023 14:31:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c183a0239ca81c05ada427d2e3ea6c6482ca40c4ab5fea745bef93398e99eb49`  
		Last Modified: Fri, 01 Dec 2023 14:31:23 GMT  
		Size: 51.4 MB (51388576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffac7166f8fc2f32b031d6c3c234c04f960b6d61d17310759c4d2c10a6ea481`  
		Last Modified: Fri, 01 Dec 2023 14:31:20 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f148edf887db25eb42ee3a349aa08deb73405e32dc10e5cbffa0b6b66431a2`  
		Last Modified: Fri, 01 Dec 2023 14:31:21 GMT  
		Size: 2.8 KB (2793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:80de990784d870b1dcf175d994d19dbcac1ab4eb172e1f134abbd975a25e3b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.3 KB (702268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc497efa88b7ff8096260c411e98013dc5a264593ff92cee73b54e51b9738845`

```dockerfile
```

-	Layers:
	-	`sha256:1f5dc483f84d137d6a5f1b622dee45feac9b76d3af1aa103c9ccd5a160a93da8`  
		Last Modified: Fri, 01 Dec 2023 14:31:20 GMT  
		Size: 672.5 KB (672514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06c6dae02792bce6554830a9806fcc358bc55b8a11e4a4928a643a509825ea7`  
		Last Modified: Fri, 01 Dec 2023 14:31:20 GMT  
		Size: 29.8 KB (29754 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:71bee62410f63c1b313d3a6b14f4ed657b448ecacb69a8098deff9ae53010b19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:5e6bef9db0bb59ded0834ccf7953b7ff4fba228c0b62f40d0dd84cf6fb929f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140560736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6a3d03b4335d3c77905757053aeb7d3b276a299ea360d049ca5319426071b2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 05 Sep 2023 23:04:32 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Tue, 05 Sep 2023 23:04:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_VERSION=24.0.6
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.0
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-x86_64'; 			sha256='6e06123399e5428fbd603564afdac74821fa0a7b4465e8a1a2359b362fc42fc4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-armv6'; 			sha256='75889ad81c5b0b07805920e398eaa7fb41c1321c81942daa07a5b5c5a1a27bdb'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-armv7'; 			sha256='2cd4af627462720384cfd2ba24d951854707d7c1fa37618c9e0319139f8a2012'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-aarch64'; 			sha256='5c09e2c6b1cd9fc1be535690ee62712687ad12f0d08b14c27d30442f0e85b955'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-ppc64le'; 			sha256='ff524f6d11050483abda01c5b1b33626c6c2f1b835df8514db6a42148d5095fc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-riscv64'; 			sha256='00302be14ad7d981eb86b834c09deb8186231b416c16454f9971bfcc0ec7e22f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-s390x'; 			sha256='323c2e92b3150ef94dc4201770e06ed7bacbe811abd77a23108cceea032fcf63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Sep 2023 23:04:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
CMD ["sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Sep 2023 23:04:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 05 Sep 2023 23:04:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
CMD []
# Tue, 05 Sep 2023 23:04:32 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Sep 2023 23:04:32 GMT
USER rootless
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636b7876979dd74729cde61aeefc7910a214801d407d5963d4941a61073c17ef`  
		Last Modified: Thu, 19 Oct 2023 01:01:01 GMT  
		Size: 2.0 MB (2014277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a3e1e7df5bfc5e27771be7f2de766c978218e4bcde12acc15bb5798bf8389`  
		Last Modified: Thu, 19 Oct 2023 01:01:02 GMT  
		Size: 16.4 MB (16390435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60190b130ff22ce63568f555059cb9e2480152ef6e7b3c11ba9f5d8610b0f660`  
		Last Modified: Thu, 19 Oct 2023 01:01:02 GMT  
		Size: 17.5 MB (17459266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce2dbd107eb0b0d892de543863087d986daaf0a2be3d440495854639f1d66e6`  
		Last Modified: Thu, 19 Oct 2023 01:01:02 GMT  
		Size: 17.8 MB (17831745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c711618a8d746c257235057f1c751090333eee8d354143f114c2031754f1f45d`  
		Last Modified: Thu, 19 Oct 2023 01:01:02 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a9d1fa736bdc93edc03d9308b756d77872cf0e8c3fea6813b0f87e13786c03`  
		Last Modified: Thu, 19 Oct 2023 01:01:03 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a915d3d782d1ec22c50998481b195e183013951efbafc92a5ca96c82f6263d0`  
		Last Modified: Thu, 19 Oct 2023 01:01:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fa7f453749db5037378a1c0410def475af9f9c17388276ab96769d4fd1ab24`  
		Last Modified: Thu, 19 Oct 2023 03:15:29 GMT  
		Size: 7.1 MB (7080495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f4a45972f0ac134ac627a1d206bb0c6f955b02f4fad3f85ec281fdc19bee7`  
		Last Modified: Thu, 19 Oct 2023 03:15:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88060cc894f1bfa624656d65dacffafc1ca354ffec59ba24af907ff01b553b0`  
		Last Modified: Thu, 19 Oct 2023 03:15:32 GMT  
		Size: 54.4 MB (54351587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e0ea80a90a76f87fb4f59157ca1269489a9d1ea1754d85209adcffa2cf40fe`  
		Last Modified: Thu, 19 Oct 2023 03:15:29 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831f6f9e30f872cbb2439fd3d439c159f11ddda39928ef70e9e7de50b9e9a52`  
		Last Modified: Thu, 19 Oct 2023 03:15:30 GMT  
		Size: 2.8 KB (2790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51331694e511817c7af194b499671898dc666d5a1246478039ac7cbe4b8bb928`  
		Last Modified: Thu, 19 Oct 2023 04:06:27 GMT  
		Size: 1.4 MB (1362179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05bb47bbc48d4359156ea4ad95b35ed79c5a16503b490d39fde39f5743dd580`  
		Last Modified: Thu, 19 Oct 2023 04:06:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6841788dd624e9c7343e25f901454d5e09cd3ad4b3c0f9418f66c503ac848711`  
		Last Modified: Thu, 19 Oct 2023 04:06:27 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729437d46a9fe2fe36b282defe38f2a4f0f39bd398b9f47b8a9ac2d5a9f4987c`  
		Last Modified: Thu, 19 Oct 2023 04:06:29 GMT  
		Size: 20.7 MB (20660322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ae4caf84a6e8590b6225b631a1bfcf10f417ce106af28c49f7eb72196effbe`  
		Last Modified: Thu, 19 Oct 2023 04:06:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6c000e6ecf7be401312530c955dc48603d0a301b2450302fbf29aba6f5e21623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.1 KB (777130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a26ec4c100e1cb1da7753bee45b48cebc2266ebf28d99d704b0735db7bcbed`

```dockerfile
```

-	Layers:
	-	`sha256:8e41c8d50b467c850c3ff7e4f049fd4a2ce5b3787fd13da5389e4759a8672bb4`  
		Last Modified: Thu, 19 Oct 2023 04:06:26 GMT  
		Size: 746.0 KB (746048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de2eee0dcd20e7a1709a88819367161618aea1ed5d944d63dd6427dc419368a`  
		Last Modified: Thu, 19 Oct 2023 04:06:26 GMT  
		Size: 31.1 KB (31082 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:42441ba25e32850da9df550a240c5583e37bf21de7190d1840dc2aeaa70fed6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133703554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a5f3b9f1aeada90e298c000d285e31ea0b29c4397c4dfaccef88eceb389fe2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 05 Sep 2023 23:04:32 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Tue, 05 Sep 2023 23:04:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_VERSION=24.0.6
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.0
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-x86_64'; 			sha256='6e06123399e5428fbd603564afdac74821fa0a7b4465e8a1a2359b362fc42fc4'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-armv6'; 			sha256='75889ad81c5b0b07805920e398eaa7fb41c1321c81942daa07a5b5c5a1a27bdb'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-armv7'; 			sha256='2cd4af627462720384cfd2ba24d951854707d7c1fa37618c9e0319139f8a2012'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-aarch64'; 			sha256='5c09e2c6b1cd9fc1be535690ee62712687ad12f0d08b14c27d30442f0e85b955'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-ppc64le'; 			sha256='ff524f6d11050483abda01c5b1b33626c6c2f1b835df8514db6a42148d5095fc'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-riscv64'; 			sha256='00302be14ad7d981eb86b834c09deb8186231b416c16454f9971bfcc0ec7e22f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.0/docker-compose-linux-s390x'; 			sha256='323c2e92b3150ef94dc4201770e06ed7bacbe811abd77a23108cceea032fcf63'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Sep 2023 23:04:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
CMD ["sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Sep 2023 23:04:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 05 Sep 2023 23:04:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
CMD []
# Tue, 05 Sep 2023 23:04:32 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Sep 2023 23:04:32 GMT
USER rootless
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecd494fa26a8aad94a0d22885340d6ee599258b2e67c6c22f91ed6221294435`  
		Last Modified: Fri, 29 Sep 2023 02:55:37 GMT  
		Size: 2.0 MB (2024548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152366591504a2012a175b6773ee6dd24c70908a8974de4f78b436134dbcd209`  
		Last Modified: Fri, 29 Sep 2023 02:55:39 GMT  
		Size: 15.4 MB (15438727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e729a1bea6f35c00510ee459c2c20ac218b3f9ddf24db1722f8ba114316a2`  
		Last Modified: Fri, 29 Sep 2023 02:55:39 GMT  
		Size: 15.8 MB (15768048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df61191e4203819ca143d9ddd941a5130452c32c2bc514644f1791119a3570b1`  
		Last Modified: Thu, 19 Oct 2023 03:14:30 GMT  
		Size: 16.3 MB (16290382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896e3ce9c2771af693c67bd4f5583b672a3f4d5db71c99447c4e6fa4700d1073`  
		Last Modified: Thu, 19 Oct 2023 03:14:29 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdedfe04474cf5b527a9af92a0a6c5bbe45194175b856d1bdceea5b72e0da24`  
		Last Modified: Thu, 19 Oct 2023 03:14:29 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf03d5960a18af5c810d08d92f517633c4c570b46f936317675110efdce962cb`  
		Last Modified: Thu, 19 Oct 2023 03:14:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c08bbdc8fb7a00d04e813bbd37b05c83fd8fe09a9899f98ace063522fb15727`  
		Last Modified: Thu, 19 Oct 2023 08:39:23 GMT  
		Size: 7.3 MB (7291334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f799874081b87c1008fb6ddada38d54110c3816fe6857dc2b31a1e797c715a1`  
		Last Modified: Thu, 19 Oct 2023 08:39:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95141bf3c415b848a1e2019d05e32b2814903d39516fae7bae08eee16fb163c3`  
		Last Modified: Thu, 19 Oct 2023 08:39:27 GMT  
		Size: 49.7 MB (49688248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d462e62db60bd9a7740ff62b858a0fa684081ba6a6a30e403feadc1863f53a8`  
		Last Modified: Thu, 19 Oct 2023 08:39:23 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c9928a90e57817b0f8dbde4ff9e5bcb105d9a7ed244ef1e185fa774c29a4be`  
		Last Modified: Thu, 19 Oct 2023 08:39:23 GMT  
		Size: 2.8 KB (2799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca473d3d6cc9b124cd49408a18f60218bcd8cb366e56a3b16e18e934228b2e1`  
		Last Modified: Thu, 19 Oct 2023 09:04:35 GMT  
		Size: 1.4 MB (1413154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973c3488b8d0250e2ae2c52cb652304a7abab1644c18e1207d9a3822bd1d17`  
		Last Modified: Thu, 19 Oct 2023 09:04:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f01a8ca69a1582ddbe39d495781d8b154de69989d89ae55e04dab61fb49ccf`  
		Last Modified: Thu, 19 Oct 2023 09:04:35 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442dfac109ba1720ef139f23f3b17d5b7f196c11075a86a842966d816b0f36dc`  
		Last Modified: Thu, 19 Oct 2023 09:04:37 GMT  
		Size: 22.4 MB (22448806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6733ab06e49858ad2a4afb9b4f52aeb72694046b855fbec5a8728e4fa51ae8d9`  
		Last Modified: Thu, 19 Oct 2023 09:04:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:34bf7fdd92e10f28722d896db78e5cd89f9251a276dece636173aaeb4c16f65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.2 KB (777203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a85afdc700cb054338ac5d23874d67d86ef33460e2762b701dd5c006e0d7a3e`

```dockerfile
```

-	Layers:
	-	`sha256:5f3f7869dda1395b108e38a74799402ec328daa66f758066ebe5c399dddfcb98`  
		Last Modified: Thu, 19 Oct 2023 09:04:34 GMT  
		Size: 746.1 KB (746061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8950340c6d28e1c91dd6419aa4a01f1690740ed770b0a9efce2e078381919c5d`  
		Last Modified: Thu, 19 Oct 2023 09:04:34 GMT  
		Size: 31.1 KB (31142 bytes)  
		MIME: application/vnd.in-toto+json

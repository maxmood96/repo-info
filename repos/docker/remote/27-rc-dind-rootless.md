## `docker:27-rc-dind-rootless`

```console
$ docker pull docker@sha256:fea5a944394eb59c9c2f80f6e335c6d74546359fb77924155db89203f7558d68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c2bb9c63057dbadff4ba57aa5e51503712ab8fb8d0821a5260e647c2536d9b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154370466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d064f6488a15855b09b2c448a666da647879dadf1751b911a89b872eb516f1c8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-x86_64'; 			sha256='2eb8de746c0bc724bb5da4de52fc9660c2e866afc9a639ffdb1adfef2649cc0c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv6'; 			sha256='ad707af427c3d3574c9e7dbc77915dcd06779a58e2c3b3783f7781166213454e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv7'; 			sha256='bd473fb4fcdb6ff9d1616d7ff3294387a574298083de91a36eed2741341f3c97'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-aarch64'; 			sha256='d95d239bec166137a1ede1d441cb808da800dacc6041c966be35066aa96c6ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-ppc64le'; 			sha256='72d4359904b6821b04b77f7dac609b994847838d1d38e5840362d64dc35d9bff'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-riscv64'; 			sha256='34f859fd5b5d3f081a88004ad9a165b01f5b549abb76e0b99a3281bc963ebbde'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-s390x'; 			sha256='d4f333a3abb6f4904e75e56196a3e6671797ef2f5e09cfbe71263f2dad466ea0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Sep 2024 16:59:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
CMD ["sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
VOLUME [/var/lib/docker]
# Fri, 13 Sep 2024 16:59:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 13 Sep 2024 16:59:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
CMD []
# Fri, 13 Sep 2024 16:59:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 13 Sep 2024 16:59:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f3e8849902084f2f3fd785bcfe58f28f8835bf59f2f5b25a75ab0241d9d319`  
		Last Modified: Mon, 16 Sep 2024 18:57:24 GMT  
		Size: 7.9 MB (7872629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e18bbc646268feb8847c371dec884f69dbdb6cc6dd82d3d678a9f14b0b6e7`  
		Last Modified: Mon, 16 Sep 2024 18:57:23 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50787d2b4edf6b87ad6e93048056ca01afc83af44554b066f5e6999311c490a`  
		Last Modified: Mon, 16 Sep 2024 18:57:24 GMT  
		Size: 18.6 MB (18562798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9499ec5416c4d35c3c91bd4fa952cf81399f35669a0a05c9addb2074f10566`  
		Last Modified: Mon, 16 Sep 2024 18:57:24 GMT  
		Size: 18.4 MB (18437712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a3ab2bac037f17e5b70fa61bd1505dd41f2b076f27ecd50358b59e72377d25`  
		Last Modified: Mon, 16 Sep 2024 18:57:25 GMT  
		Size: 19.0 MB (19036016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca6043529f1d90d9198762a2fc42c643a2b8d5d5beddf93fae123e6bc1727a`  
		Last Modified: Mon, 16 Sep 2024 18:57:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af26356b05f6365c8d5f8bbc9202fffbaf0cf6893bdcdaba1dd028348c61625`  
		Last Modified: Mon, 16 Sep 2024 18:57:25 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c6e3a6117f962dfec48fd6240b6c794c49889772f0e08f2dbb8542001011af`  
		Last Modified: Mon, 16 Sep 2024 18:57:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3f58ef6cda3c2ccb41117e89dc3841183fa88e2155cf5bb37ff3c59c93c365`  
		Last Modified: Mon, 16 Sep 2024 19:50:39 GMT  
		Size: 6.7 MB (6657938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eb679090d24286d366436b81b3bd3902262014815ed042c13b122bb0fd0d2f`  
		Last Modified: Mon, 16 Sep 2024 19:50:39 GMT  
		Size: 89.2 KB (89219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390fc7e846729cc3d359442ffe4fcbbd6ae7f165d66e6ac9fdc68542586725da`  
		Last Modified: Mon, 16 Sep 2024 19:50:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4437419100c42fca27189dbe618401d139be05bf75054985fd7fbdce9d921cb2`  
		Last Modified: Mon, 16 Sep 2024 19:50:40 GMT  
		Size: 57.8 MB (57796832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab71e97f3a0dafba74c022094c065ad70f5de9eaa3be6daef3013b1c99f4ef30`  
		Last Modified: Mon, 16 Sep 2024 19:50:40 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e9829c5b4b8bbd47f177dcb41cb63dd763fbcc72cdd840c9215b653922a726`  
		Last Modified: Mon, 16 Sep 2024 19:50:40 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcb595d782d3c0c07407253cabc01317c04c66ee317992594d5df8002d29ab5`  
		Last Modified: Mon, 16 Sep 2024 20:48:59 GMT  
		Size: 981.0 KB (980973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc855c0a5d0d467873474cb29608a1f781a875629d816dc4fd43d3793c44aaed`  
		Last Modified: Mon, 16 Sep 2024 20:48:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3e9e32de7bc929a40ee95f28cdc2ded3661c0510cffa42370db2ba9a73b4b9`  
		Last Modified: Mon, 16 Sep 2024 20:48:59 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a743e874eec7c66215dad9be1d0228d7579deed125215d93c0baa28b107bed65`  
		Last Modified: Mon, 16 Sep 2024 20:48:59 GMT  
		Size: 21.3 MB (21303246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b9b9e2fb32f25ce450f3f5d6566cdb75ab105a632db8cf9fdf4fadf2a950bf`  
		Last Modified: Mon, 16 Sep 2024 20:48:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:36d0ad9a69dedc85c985fbab1f837708e8ae0c04a718b424be4fb607999ab57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e1cd5ed1092db0b842101dc2b8675f115e66fa849b52d09d680fc3b6ae7860`

```dockerfile
```

-	Layers:
	-	`sha256:4a3164247ad086076cbc94cdce68a25e006e787ba8443b09ed277be313c03aa3`  
		Last Modified: Mon, 16 Sep 2024 20:48:58 GMT  
		Size: 30.3 KB (30332 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b5f6e358e2a67823db93a76872fe2e59bd9c117c711f5784f893a7e7bbd32b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148547975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc83b71333818a0e7a4ca928e68aa9d1be25e500b7db41f503192a723b3c570`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.4
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-x86_64'; 			sha256='2eb8de746c0bc724bb5da4de52fc9660c2e866afc9a639ffdb1adfef2649cc0c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv6'; 			sha256='ad707af427c3d3574c9e7dbc77915dcd06779a58e2c3b3783f7781166213454e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-armv7'; 			sha256='bd473fb4fcdb6ff9d1616d7ff3294387a574298083de91a36eed2741341f3c97'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-aarch64'; 			sha256='d95d239bec166137a1ede1d441cb808da800dacc6041c966be35066aa96c6ee7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-ppc64le'; 			sha256='72d4359904b6821b04b77f7dac609b994847838d1d38e5840362d64dc35d9bff'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-riscv64'; 			sha256='34f859fd5b5d3f081a88004ad9a165b01f5b549abb76e0b99a3281bc963ebbde'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.4/docker-compose-linux-s390x'; 			sha256='d4f333a3abb6f4904e75e56196a3e6671797ef2f5e09cfbe71263f2dad466ea0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 13 Sep 2024 16:59:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
CMD ["sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
VOLUME [/var/lib/docker]
# Fri, 13 Sep 2024 16:59:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 13 Sep 2024 16:59:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 13 Sep 2024 16:59:50 GMT
CMD []
# Fri, 13 Sep 2024 16:59:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 13 Sep 2024 16:59:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 13 Sep 2024 16:59:50 GMT
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
	-	`sha256:df7ab6a65b5548b28c6ea479b5fa1d0e59628b777830db0afcafd60fb3ea2a24`  
		Last Modified: Fri, 13 Sep 2024 18:56:10 GMT  
		Size: 17.5 MB (17515930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e4860376f01b29ad074f91764ce3a106a4766d66e3c0a722484baa53bd66bb`  
		Last Modified: Fri, 13 Sep 2024 18:56:10 GMT  
		Size: 16.8 MB (16800754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bc06bbb608b659faa9cf501ca521a2bff1d6fdf0b1eb5ba639440eaacd3082`  
		Last Modified: Mon, 16 Sep 2024 18:56:52 GMT  
		Size: 17.4 MB (17414619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6614f199bee42d7d7b3d7dfee2213e58aff9315205b9fcc2477720b315e847c8`  
		Last Modified: Mon, 16 Sep 2024 18:56:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16659473e6476b5eabc21aef8600620379c9b3137e0621ddaea3e5f48235b2d`  
		Last Modified: Mon, 16 Sep 2024 18:56:52 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f17af642346b11ac3e8799b8da4d53595252fda7daaa3c78e124744c2faad9`  
		Last Modified: Mon, 16 Sep 2024 18:56:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aead99a6b713e9ca19a6543baae650c9893f2af35a6d52cc0fa2f602c510afa1`  
		Last Modified: Mon, 16 Sep 2024 19:50:27 GMT  
		Size: 7.0 MB (7034888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da8a69120ac6a3d698733693b56c8bdff38ff488ebdbf3471e78ad250ede33f`  
		Last Modified: Mon, 16 Sep 2024 19:50:26 GMT  
		Size: 98.6 KB (98649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f776b0578802e9c8844c0e21776839605a746a34e2257d0c4cf8cae80e97a6`  
		Last Modified: Mon, 16 Sep 2024 19:50:26 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4838935aea1b9bf9bc82dde98232c335ace6a476f8fdabc25348358bc890139f`  
		Last Modified: Mon, 16 Sep 2024 19:50:28 GMT  
		Size: 53.4 MB (53425704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7582bd015b84261d524121bfcdbb243350bf2d553d74fbb6340e5f091a8d38`  
		Last Modified: Mon, 16 Sep 2024 19:50:27 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a16cd334a9a43e067cd6a81f21708bc31e640ee2edca9db61687ebad52ee7b`  
		Last Modified: Mon, 16 Sep 2024 19:50:27 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc00eb4e3e384578a58d89718da8d083437783e2bc5efdd88b42b20737d7563d`  
		Last Modified: Mon, 16 Sep 2024 20:48:59 GMT  
		Size: 1.0 MB (1023106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42daaee5e028c48c0e843c4ffa3206c6a4f0389606bfcb5d25264671b5a26a4`  
		Last Modified: Mon, 16 Sep 2024 20:48:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37e3948a7dc85fa0ed5166a7482dc8574de8eec2c6827899ab3e58cc8867d90`  
		Last Modified: Mon, 16 Sep 2024 20:48:59 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96679614d2498ed37eb1a6b34ac0d984527fd01bf374fa47c253e93cba3847c9`  
		Last Modified: Mon, 16 Sep 2024 20:49:00 GMT  
		Size: 23.2 MB (23155434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c61062303fe2b968c92866a84b62c33afe67eaf1ffa376c49eb862eadbb9ca`  
		Last Modified: Mon, 16 Sep 2024 20:49:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:167012afc9c95f61cc8c7b38a6a20c6b4fb83c6bfdc03d023b8ab83036460f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c54f09976cb7b3636790603d2aefe52eb90d6b5738defc33dc76775cd2ff1ee`

```dockerfile
```

-	Layers:
	-	`sha256:91d0ce864623fb427c8467c101a43140e07d75f04bc5eb0b8bb9c026e28e8686`  
		Last Modified: Mon, 16 Sep 2024 20:48:58 GMT  
		Size: 30.7 KB (30746 bytes)  
		MIME: application/vnd.in-toto+json

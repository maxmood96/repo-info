## `docker:dind`

```console
$ docker pull docker@sha256:eb59696588157b44998ec085a1373fa0966a5e2cac8c42305cce085d1ef7adf0
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

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:96e0ecc1b024d393519f4bb53ac68fcd3caf0025b61c2c110b71ff82f960aa6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118405953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea1eb0176b7489ad72d62971a3639e85892ddf76bfc6645b4aabd56466814cf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_VERSION=24.0.7
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 Dec 2023 18:52:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
CMD ["sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
VOLUME [/var/lib/docker]
# Fri, 15 Dec 2023 18:52:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 Dec 2023 18:52:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
CMD []
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53a859d716d847246628ec5f739d4d7f6c1728f55c205abd1598f2961a2c971`  
		Last Modified: Fri, 05 Jan 2024 01:53:58 GMT  
		Size: 2.0 MB (2018457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf01e7f8edca3a0012a20af11f8c2f7be6c2c902de3981ed32bc6ebad2655716`  
		Last Modified: Fri, 05 Jan 2024 01:53:58 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1c0178eca3693c4ce0502dd216fae6def1dfa4497af2f0d680f888c3a3448a`  
		Last Modified: Fri, 05 Jan 2024 01:53:58 GMT  
		Size: 16.4 MB (16400387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bfe81a0ee4e5a2ebbac7ff0b76da9dd5ba83575c207e2b02877fb9e2054034`  
		Last Modified: Fri, 05 Jan 2024 01:53:58 GMT  
		Size: 17.2 MB (17195289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cf4974ce8787b54ac0af681cd7f519e3864bd9556ab69f588c33fa58175918`  
		Last Modified: Fri, 05 Jan 2024 01:53:59 GMT  
		Size: 17.9 MB (17852058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28675e076aedbe9776450e25ab7891c5e4a1478ae05a8cc51c67d40be2454b7d`  
		Last Modified: Fri, 05 Jan 2024 01:53:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afea6457077a569f2c37e45b0300ddb42b1c081c1c00b07bf504f78ef68831d8`  
		Last Modified: Fri, 05 Jan 2024 01:53:59 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9082a5a0c9c3065e4969dca03f10a9357bc7c8bc7e4ea8d0f26c1eb10bc65841`  
		Last Modified: Fri, 05 Jan 2024 01:54:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627355d18acfe4a8595155195a858a25aa23bed0ac6d327969741ea18eee5f50`  
		Last Modified: Fri, 05 Jan 2024 05:47:45 GMT  
		Size: 7.1 MB (7068075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5016005cf30aedc93ae4552413b24460694e8d967db8901737ff5cfb48d2ef1`  
		Last Modified: Fri, 05 Jan 2024 05:47:45 GMT  
		Size: 83.6 KB (83640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e562a30a7b4b772e793e0f66b6acb764f11597ad580a85ea19509da2492cffb1`  
		Last Modified: Fri, 05 Jan 2024 05:47:44 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d11eb5abc4fb04c6d69ea5190da668785405b4eb3dbe646cbdd3bf04f12dd8`  
		Last Modified: Fri, 05 Jan 2024 05:47:46 GMT  
		Size: 54.4 MB (54371626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22971a72bb2ad832c6210c5868fde7003604c71d2f18a2ca140a56e6916e6dfa`  
		Last Modified: Fri, 05 Jan 2024 05:47:45 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ad04e5d4efc7caeb460ec550cdcbae188555d812679ed23799f001fdc98e37`  
		Last Modified: Fri, 05 Jan 2024 05:47:46 GMT  
		Size: 2.9 KB (2873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:c3404dbe8e9da462219c3cd830f013c986f0ea630cdcf33a01dd532c878ab2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.6 KB (720609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6c36d18534e357045444a92f241a2363924ba1ed0a27122f30b57a8be4f93d`

```dockerfile
```

-	Layers:
	-	`sha256:9fb49f063c88da41c3201f2c4bb5ddfd7ae19d1c86d2beef0487bb22b084bbad`  
		Last Modified: Fri, 05 Jan 2024 05:47:45 GMT  
		Size: 683.6 KB (683626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87d2552527111804a93bd2c63f8f2246bbc26cfd28b68765a52e20cd818d5505`  
		Last Modified: Fri, 05 Jan 2024 05:47:44 GMT  
		Size: 37.0 KB (36983 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:003c7e14b7022766d273fb4fa348b25830f9b49c561d0eefebb1dbcc1f83d12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111790712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4db86896958d6d46172a126e47d66e0a502f250692a915163397d218540475`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_VERSION=24.0.7
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 Dec 2023 18:52:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
CMD ["sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
VOLUME [/var/lib/docker]
# Fri, 15 Dec 2023 18:52:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 Dec 2023 18:52:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
CMD []
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc5bd010434069cd814513c40515b0b34d950c4606c108f726b20bc580362b6`  
		Last Modified: Fri, 05 Jan 2024 22:45:12 GMT  
		Size: 2.1 MB (2108662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbc809bdc4cc776e79e9ae1a93a9fed1e6438a007c9fc5f7a92f34cfbaa9fb4`  
		Last Modified: Fri, 05 Jan 2024 22:45:12 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bd0d5d8eb48f81abbfaa7c70409f739d235f25293f0bc2ac09997cac957a27`  
		Last Modified: Sat, 06 Jan 2024 01:47:42 GMT  
		Size: 15.1 MB (15132562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b028388004f00244e4a17457a11711234a2b84e4d33e250284d85c62e53a1fcc`  
		Last Modified: Sat, 06 Jan 2024 01:47:42 GMT  
		Size: 16.1 MB (16099965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ecf1742b110f0f7bd6ccd01419e68921f32aa62478ab255b1da503d6f5866f`  
		Last Modified: Sat, 06 Jan 2024 01:47:42 GMT  
		Size: 16.9 MB (16867519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6af86c77adb225e63b11f16f53ab4aaf8ae0e44a8518c564b07155e4fc8671`  
		Last Modified: Sat, 06 Jan 2024 01:47:41 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722bb4aa882f7e95451704f6190c92b1dba17ad71e37485883863941d3b6177a`  
		Last Modified: Sat, 06 Jan 2024 01:47:42 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b126e325c1b02440c0b9f710295e73e80656036ab2b55c1b74625e8a587729`  
		Last Modified: Sat, 06 Jan 2024 01:47:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ae0da82b0de439e9cb292a440aff71ec0f3657b905bd0f75e1344c91a4b203`  
		Last Modified: Mon, 08 Jan 2024 01:28:32 GMT  
		Size: 7.4 MB (7361988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ce33a02ffbb70f1cdf499e369a140047856db734762a68ba79cd21524ec635`  
		Last Modified: Mon, 08 Jan 2024 01:28:31 GMT  
		Size: 82.6 KB (82597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fa5cee90867babf26b22c3e1bab0163bbb6fe3ff3846e9dfde4afb73a41c51`  
		Last Modified: Mon, 08 Jan 2024 01:28:31 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b04a8ffa95f7862d09c8f9df69abd9c09b4c5741eff2e7dfbdcf61a63a420`  
		Last Modified: Mon, 08 Jan 2024 01:28:33 GMT  
		Size: 51.0 MB (50964337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71f3999c1962e85994b34af1814bde67f415e04fad3600c823b9a38128f24d6`  
		Last Modified: Mon, 08 Jan 2024 01:28:32 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3ab13f5cf94d4316294ad84e7b4ade8567997c1a21d48355eaad809f8dec8d`  
		Last Modified: Mon, 08 Jan 2024 01:28:33 GMT  
		Size: 2.9 KB (2869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:fdb3252a0f8751a94fb5fb1b030b8f4218447b3cceefce37c2b8e9d08b434832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00313da04f8ce6e7e35ae80cd41b03be62156f8c4329277e3426105c6779dac3`

```dockerfile
```

-	Layers:
	-	`sha256:88e31180a940e2cba166d83606c0e474b8ed07f8e36b4e8c35f5c1821fa0f7fe`  
		Last Modified: Mon, 08 Jan 2024 01:28:31 GMT  
		Size: 36.9 KB (36943 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a9b83ae64726a16009c6bed526a7af9069498f21802c71a5e31c016459ba1179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110572391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd8f4e823d563d0bf38c4cd2a4292f6ea5767bef49f95423c7a00d658bb9e52`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_VERSION=24.0.7
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 Dec 2023 18:52:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
CMD ["sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
VOLUME [/var/lib/docker]
# Fri, 15 Dec 2023 18:52:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 Dec 2023 18:52:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
CMD []
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f7102b17e4ec828559672f3388bba1ec86d87e7aa09caba4b82fc6870b4fa6`  
		Last Modified: Thu, 14 Dec 2023 22:03:12 GMT  
		Size: 1.9 MB (1888652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f19fa8a6c45d74eb65c7d5844869fef846c8305dd15e21604b2c06e20d1279`  
		Last Modified: Fri, 05 Jan 2024 02:27:22 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a2c3757bdf650079318e50948f607eeba62f86de7a267fdbfb2a7e87d9a101`  
		Last Modified: Fri, 05 Jan 2024 02:28:04 GMT  
		Size: 15.1 MB (15127047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c4e359b38f7426061b0727164359f0d5f884f73f79b80098a6ee102dee5fc8`  
		Last Modified: Fri, 05 Jan 2024 02:28:04 GMT  
		Size: 16.1 MB (16084084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a525a3e7425c74a565af54215e5a8872ac93e5bbcefabd46bb7b9dc1a052ac`  
		Last Modified: Fri, 05 Jan 2024 02:28:04 GMT  
		Size: 16.9 MB (16852952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b69a1e5778094df8ca1378183d1f04ba65326f5835d82177fc35c4ad7df4b6`  
		Last Modified: Fri, 05 Jan 2024 02:28:04 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b799b82195526901d3b7c052677b14bda1ed5f44110d27b2ad55afaa39dae8`  
		Last Modified: Fri, 05 Jan 2024 02:28:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d13342bb39d8a15fc898f727b626dae348431acee94e28ed004ef89d3cd39b`  
		Last Modified: Fri, 05 Jan 2024 02:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f936a1603febff0326f07e5e83f64210dcd7b7267e6f89789f887c02f014fb3e`  
		Last Modified: Fri, 05 Jan 2024 06:51:30 GMT  
		Size: 6.6 MB (6649779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfea5914c1b7d765386b03ad795aa0813c76280aef8b0ffcc78e3d456af9187`  
		Last Modified: Fri, 05 Jan 2024 06:51:30 GMT  
		Size: 78.9 KB (78879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fb4d8f54d168feb2c67e7cea23a43c798568e9ac7f3401e242aee1d6094ba4`  
		Last Modified: Fri, 05 Jan 2024 06:51:30 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b77a7dce0ad6a3e7775874b251c388ded6d2733c9597b7c9bc6aa86732e01d`  
		Last Modified: Fri, 05 Jan 2024 06:51:32 GMT  
		Size: 51.0 MB (50964364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78c5a1e8e0af2f8dfa62cc36408ccb43b211bf5b96c20f636f0f55cba792c78`  
		Last Modified: Fri, 05 Jan 2024 06:51:31 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b269b72cefaaf10c40f075f4e90a54c826dfd6136655b9e4c73f4e96aec499`  
		Last Modified: Fri, 05 Jan 2024 06:51:31 GMT  
		Size: 2.9 KB (2870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:9ae94977a6b27f097077f0a397a989945c0b05dbc57ed9e285e422444e1fe969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.9 KB (720917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d41895c8c8abfc3028b5411904b1233cd7fcac5a185594795e471e6126bf76`

```dockerfile
```

-	Layers:
	-	`sha256:4f1dde198d3fb1dc75421aa9f8d71d84645e964c8a3f00db5251fa7d81a999cf`  
		Last Modified: Fri, 05 Jan 2024 06:51:30 GMT  
		Size: 683.7 KB (683710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ceb3fa83e894c5c2d8995d70b7a127653ff29e55e6809fe9fc04c23ddac7d9`  
		Last Modified: Fri, 05 Jan 2024 06:51:29 GMT  
		Size: 37.2 KB (37207 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4bbb1ca75dd420ee602eb36cd142fa7465009893f053298f59c899cd97bc5e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109995875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef69a97cd09246ad7093f89f8afd8fa5e438fbb41722b54b6c6c591a55cbcf5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_VERSION=24.0.7
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 15 Dec 2023 18:52:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
CMD ["sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 15 Dec 2023 18:52:20 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 Dec 2023 18:52:20 GMT
VOLUME [/var/lib/docker]
# Fri, 15 Dec 2023 18:52:20 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 15 Dec 2023 18:52:20 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 15 Dec 2023 18:52:20 GMT
CMD []
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4959de38143abac793d31e4e8592696721305ff06281f8b9284aee380afcfe`  
		Last Modified: Thu, 14 Dec 2023 22:04:39 GMT  
		Size: 2.0 MB (2014899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf613c8d3eefad31faacee38beeedf68069e48ea01d8f083fa0a57ce343ed827`  
		Last Modified: Fri, 05 Jan 2024 02:15:00 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904cd2aef7e75dfb117f3229ae16a845ec7fc5a531dc4703c9570b506ea21c29`  
		Last Modified: Fri, 05 Jan 2024 02:15:27 GMT  
		Size: 15.4 MB (15449542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e44a629b948c47ee6da1de5e92365267b4b537fe5fad7bfda80adb3e3f5518`  
		Last Modified: Fri, 05 Jan 2024 02:15:27 GMT  
		Size: 15.6 MB (15640605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04298b4e6756d10ff289aaf3ecd71e35a76893d2d0896c9bfb14e81246ec448`  
		Last Modified: Fri, 05 Jan 2024 02:15:27 GMT  
		Size: 16.3 MB (16302331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db00625aa31c36fd07b00a42fdc96f86e019cd92b3fb6c78893737e23aefc440`  
		Last Modified: Fri, 05 Jan 2024 02:15:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fbfa586ea4aa82277160546ce02d4693104a660a28fc41a3c6012be35dc9d2`  
		Last Modified: Fri, 05 Jan 2024 02:15:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f0179b0d1729e72edf34c7bdbbc54a11dddced0d7d5a937a104b39f4d74f3`  
		Last Modified: Fri, 05 Jan 2024 02:15:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c888c82111fa29af8888fb20ea00263fb193bb333c0e07598bd2ffb8c19ad53`  
		Last Modified: Fri, 05 Jan 2024 06:15:10 GMT  
		Size: 7.4 MB (7428479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d864b1096e775d8b77215c9453fd27837d89862fb34052920420260f1c46db80`  
		Last Modified: Fri, 05 Jan 2024 06:15:09 GMT  
		Size: 93.1 KB (93068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c9c04c7c50d5d1563eb06e931bb544ee9307658850a497e3cef850c7fbc4ad`  
		Last Modified: Fri, 05 Jan 2024 06:15:09 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91812c08847e4b8a9fac6febf66b6737a798f5a87ff6f00081bfe3b391d7e65f`  
		Last Modified: Fri, 05 Jan 2024 06:15:11 GMT  
		Size: 49.7 MB (49711214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe041380c5e8ee783d23426da30de77a9331666e65c6b8da2e16f823311f249`  
		Last Modified: Fri, 05 Jan 2024 06:15:10 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dbce499e9f250417d23cef9b758e472c2f8a7f788f181744c29bf022542fe1`  
		Last Modified: Fri, 05 Jan 2024 06:15:10 GMT  
		Size: 2.9 KB (2874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:e557ee5d1e80ee200c47ec20473f5c1184574d682bbef4d000f3b8bcb13d9080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.7 KB (720708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0937459e2e20cb4c785096b0639f42bed71fd8422fc70104d55f3bad6391b2`

```dockerfile
```

-	Layers:
	-	`sha256:f9c0948065dad82bdd678b536dae5c77c4d0fbf83902bfeb72964ff442aab5fd`  
		Last Modified: Fri, 05 Jan 2024 06:15:08 GMT  
		Size: 683.6 KB (683649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43871d6d3ebd8cbb0d389da51089a6d59e3e0737a5005f559f71fddb2d7bc128`  
		Last Modified: Fri, 05 Jan 2024 06:15:08 GMT  
		Size: 37.1 KB (37059 bytes)  
		MIME: application/vnd.in-toto+json

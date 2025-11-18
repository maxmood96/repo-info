## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:a2724f8107a4130ed902787a45b74c5ccb8f2022e42ce47c9b00c57067b8107f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:f9ac10d657597d94be173a95ac886a5b63d1a1835c95f1872f642dd46fc35c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164699680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea37dcb021cc0171910797822a8bec3b5b4305b0da180dafea0c1df5d42a8c24`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:52:01 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 10 Nov 2025 19:52:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 10 Nov 2025 19:52:01 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 10 Nov 2025 19:52:05 GMT
ENV DOCKER_VERSION=29.0.0-rc.3
# Mon, 10 Nov 2025 19:52:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 10 Nov 2025 19:52:05 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Mon, 10 Nov 2025 19:52:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 10 Nov 2025 19:52:06 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Mon, 10 Nov 2025 19:52:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 10 Nov 2025 19:52:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 10 Nov 2025 19:52:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:52:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 10 Nov 2025 19:52:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 10 Nov 2025 19:52:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:52:08 GMT
CMD ["sh"]
# Mon, 10 Nov 2025 19:58:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 10 Nov 2025 19:58:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 10 Nov 2025 19:58:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 10 Nov 2025 19:58:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 10 Nov 2025 19:58:13 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 10 Nov 2025 19:58:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 10 Nov 2025 19:58:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:58:13 GMT
VOLUME [/var/lib/docker]
# Mon, 10 Nov 2025 19:58:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 10 Nov 2025 19:58:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 10 Nov 2025 19:58:13 GMT
CMD []
# Mon, 10 Nov 2025 20:10:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Mon, 10 Nov 2025 20:10:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 10 Nov 2025 20:10:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 10 Nov 2025 20:10:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-29.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-29.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 10 Nov 2025 20:10:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 10 Nov 2025 20:10:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 10 Nov 2025 20:10:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0550213a2a661c86919e23e71adaac14c8a2357b0d9474b1b4ffde2e494c6aae`  
		Last Modified: Mon, 10 Nov 2025 19:52:25 GMT  
		Size: 8.2 MB (8232193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ff214b46477cf55a39eb8a64ba8c4c59a409f5da52cf9c9f3d2ae1d2111661`  
		Last Modified: Mon, 10 Nov 2025 19:52:24 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0934e37672c8b037a2225fe7556b5de23f6a85974db4e7465f73af4a4efd167d`  
		Last Modified: Mon, 10 Nov 2025 19:52:29 GMT  
		Size: 18.7 MB (18729569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c4e775fbfc332a827cfbcb0dec1ed3490b757474a6adf58b83e5d7ece7033a`  
		Last Modified: Mon, 10 Nov 2025 19:52:30 GMT  
		Size: 22.2 MB (22158453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c324a4a19f13c93bd4af0c5de305da388b1d48d2e910de245ec8ce0b4d9098`  
		Last Modified: Mon, 10 Nov 2025 19:52:27 GMT  
		Size: 21.7 MB (21744275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c6fc60f9981961c8b16caa7a2d18b2346f770ffbb66fe3fa018654b280f694`  
		Last Modified: Mon, 10 Nov 2025 19:52:26 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90c8dc54ed8cfdb6160b0f471cd0678ef865fb1807d2719cf77b0a51b7df324`  
		Last Modified: Mon, 10 Nov 2025 19:52:26 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522784886b78ca409cba8a62a8d6f57c2197a698a38e5556b0d3a35fac95c677`  
		Last Modified: Mon, 10 Nov 2025 19:52:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aefb0dfdbf4b91f7757ef672e0d35a3b11aa517885d56804c39a0c643ae6453`  
		Last Modified: Mon, 10 Nov 2025 19:58:31 GMT  
		Size: 6.9 MB (6905446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa40a39c68c527a7fb0154fae0fdd8c199c66fd6c753cf69f534359e3304c1b3`  
		Last Modified: Mon, 10 Nov 2025 19:58:30 GMT  
		Size: 90.4 KB (90379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c053b02724c93b6a3be1b765a36067971f7978172a9b0401cbdf18259a2d221`  
		Last Modified: Mon, 10 Nov 2025 19:58:30 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2fc60ebfb8bcc9c633212e7cead29d05e652bfc430b6d3cf96ef58e96f1716`  
		Last Modified: Mon, 10 Nov 2025 19:58:37 GMT  
		Size: 62.3 MB (62258796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87491bff1f6d67980489cd559d7e39032808c77966df733b0b2260e94007db0d`  
		Last Modified: Mon, 10 Nov 2025 19:58:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8906c1a967b450199f22e4c63aa027baa716c41991b860a32ce116c4d895d8ff`  
		Last Modified: Mon, 10 Nov 2025 19:58:30 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd2518760282ddc363f2c2b81658438cfdc88cc33d544c3a73385fa6dd98989`  
		Last Modified: Mon, 10 Nov 2025 20:10:42 GMT  
		Size: 3.4 MB (3398393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e89312486e76164d638a55f9d33787d1675e2ff3ae037cb7a64db59fbb4594`  
		Last Modified: Mon, 10 Nov 2025 20:10:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885836a482d0b19823d463fbe14ed388c70e2030fca5fb5ed10d3dbb006fbe09`  
		Last Modified: Mon, 10 Nov 2025 20:10:41 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8562080653b8e02d49591c630b570a4e271f04cc292b466c59e23c72cb8e9223`  
		Last Modified: Mon, 10 Nov 2025 20:10:43 GMT  
		Size: 17.4 MB (17370237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4222117c245d4a0080dbcb2beb6f32c2b831d29d33319a5a251304c47acc2074`  
		Last Modified: Mon, 10 Nov 2025 20:10:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:71a4f96a5b83b4463565efa8f0e645f0f7adcb5dbb07b84759bc37ea8d255b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6965e3708071f40ee23178cfee5dba20aac662dd42ea534df31d2882f2d80985`

```dockerfile
```

-	Layers:
	-	`sha256:33673ff894bbd5471b71da5c73f80b0a77a89c73f02d113d455aef007c4e1692`  
		Last Modified: Tue, 11 Nov 2025 00:07:46 GMT  
		Size: 30.3 KB (30346 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cfc066c18eca80708ea180af5f2b4be451fe7207da89566b057885eed27f59bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154683517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f07a96199a095babd9d0949eacfaed74b0c7a788d684f5fafca9d64189ebedd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:52:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 10 Nov 2025 19:52:30 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 10 Nov 2025 19:52:30 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 10 Nov 2025 19:52:35 GMT
ENV DOCKER_VERSION=29.0.0-rc.3
# Mon, 10 Nov 2025 19:52:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 10 Nov 2025 19:52:35 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Mon, 10 Nov 2025 19:52:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-amd64'; 			sha256='7d2d7d6d4680aa349614965aaa33ccec43f1a9a21e908a5ce4cb6adfa5ad5141'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v6'; 			sha256='37d0aeef65766de8e1d053210fb1f062e01a44c34a65a118a7e7942cbbf68cab'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm-v7'; 			sha256='ba46e94d7420b4b05ff02109f5f8a937a86a620a660898ff15fb987022f62588'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-arm64'; 			sha256='50e85c4e290b698908421161c1aee069bcc5d4a65b7b7201bfac3a176b223a7e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-ppc64le'; 			sha256='04e9b85273502f5c673f2216f64fe336045b6d196ba7e0350a11d6af5dcaee3a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-riscv64'; 			sha256='f4f2d5bd103b8bba725b3b0ef14e9a4a799e0806d5076045e399e221a3bbb723'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.linux-s390x'; 			sha256='3b5caf470972c286642112df47b2251d2a5d412aa150d78d74db20a3409d9f23'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 10 Nov 2025 19:52:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Mon, 10 Nov 2025 19:52:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 10 Nov 2025 19:52:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 10 Nov 2025 19:52:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:52:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 10 Nov 2025 19:52:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 10 Nov 2025 19:52:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:52:37 GMT
CMD ["sh"]
# Mon, 10 Nov 2025 19:58:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 10 Nov 2025 19:58:19 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 10 Nov 2025 19:58:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 10 Nov 2025 19:58:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 10 Nov 2025 19:58:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 10 Nov 2025 19:58:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 10 Nov 2025 19:58:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:58:22 GMT
VOLUME [/var/lib/docker]
# Mon, 10 Nov 2025 19:58:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 10 Nov 2025 19:58:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 10 Nov 2025 19:58:22 GMT
CMD []
# Mon, 10 Nov 2025 20:13:53 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Mon, 10 Nov 2025 20:13:53 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 10 Nov 2025 20:13:54 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 10 Nov 2025 20:13:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-29.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-29.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 10 Nov 2025 20:13:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 10 Nov 2025 20:13:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 10 Nov 2025 20:13:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5956c1cee872b51395d4b0a5434ec4f12f9e92d4bd8c2477f2fe7c2f2515f4`  
		Last Modified: Mon, 10 Nov 2025 19:52:53 GMT  
		Size: 8.3 MB (8257256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53472fa28cc5a4e39fca6fe43d60ef62228fea7f2f95864fd874d9fa256f4402`  
		Last Modified: Mon, 10 Nov 2025 19:52:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3d560d270611a6601a128f3e2b1fd7a46116f5adbbaf0431b16f0f6bd93d7f`  
		Last Modified: Mon, 10 Nov 2025 19:52:53 GMT  
		Size: 17.3 MB (17305453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48656f54e50e49f978027edcc46cf763f62c0334eafa041ac9dd83d7ff6f800`  
		Last Modified: Mon, 10 Nov 2025 19:52:54 GMT  
		Size: 20.3 MB (20273411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819b0b62ddd61a81413d3c74954989c6a82884f497e7f8f1317ffb2b09bb1f40`  
		Last Modified: Mon, 10 Nov 2025 19:52:53 GMT  
		Size: 19.9 MB (19869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd952c6a19d74a0ba32c15f6b4832562ae567f3322f8a1c6649df2eda65ad8dc`  
		Last Modified: Mon, 10 Nov 2025 19:52:52 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873a3491b3240277ccce4802d312fb297c8c7c8761b3209b869483f56f0c2919`  
		Last Modified: Mon, 10 Nov 2025 19:52:52 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab6612004f3bf119a22672719ab7ae2035a06c6ce493a17362c193a7bee987a`  
		Last Modified: Mon, 10 Nov 2025 19:52:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cea3a143210f60bdfe31f65eb926b77a7e1d1cf6bdde0bd8402a94fcedf8b65`  
		Last Modified: Mon, 10 Nov 2025 19:58:40 GMT  
		Size: 7.1 MB (7140868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2714949339e1fd02e16c85ee6b8580cd2bbd0d31f5750a84db850b3a65ce14`  
		Last Modified: Mon, 10 Nov 2025 19:58:39 GMT  
		Size: 99.5 KB (99500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e59f0c412ca9dbcdd0ee42c65e686f20fcf155007fcc5036d439ca6b2e01bc1`  
		Last Modified: Mon, 10 Nov 2025 19:58:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01448e4b7c427e5ea3a53137935d0b85ab4f271b69916702eb6db184ba2f83`  
		Last Modified: Mon, 10 Nov 2025 19:58:45 GMT  
		Size: 56.5 MB (56492615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bc44a49061bf5f403fe40afdf0965691b5fa4b8c8c9be3079522bd6f87e89b`  
		Last Modified: Mon, 10 Nov 2025 19:58:39 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b20069f23ed42d9687f3c6f2d0aa67f2838e0a241876bc81be3c668694428b`  
		Last Modified: Mon, 10 Nov 2025 19:58:39 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7777a4b690199bc20ac7efe257f35a8a177826dfb22eb2308774ca25daec97fb`  
		Last Modified: Mon, 10 Nov 2025 20:14:08 GMT  
		Size: 3.4 MB (3389945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9d8901f246fa4fe7e52c5093368c52253a428e50bf17c80d58fc55be97db1`  
		Last Modified: Mon, 10 Nov 2025 20:14:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f98883fdd5bda5b7035673ced511a8ca2bd7220cf3ef1e83b1bb2d8483c1588`  
		Last Modified: Mon, 10 Nov 2025 20:14:08 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e0d36e79e2f9cdd2dce4265f94e1c30354773a983df4aa8ed3802f5960fb1b`  
		Last Modified: Mon, 10 Nov 2025 20:14:11 GMT  
		Size: 17.7 MB (17707041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8f8645d9c2407fce4ae0fd88bbb5a4ee285221b1ab3a4f7986330e3e4bf5a7`  
		Last Modified: Mon, 10 Nov 2025 20:14:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c5f0a992dade110ce6dc9b06f0f2b8267dc66752b24fa27f7de5881b7cd5669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcaf7ab13637eea13935ebb335448c20a12fad67780b24d15b7184eee8b9f14`

```dockerfile
```

-	Layers:
	-	`sha256:312a27c581bef60ececfcbf7891452ecc656de5ecc4b4453c8644fcb743d3cd9`  
		Last Modified: Tue, 11 Nov 2025 00:07:52 GMT  
		Size: 30.5 KB (30498 bytes)  
		MIME: application/vnd.in-toto+json

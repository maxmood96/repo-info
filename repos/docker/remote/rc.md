## `docker:rc`

```console
$ docker pull docker@sha256:2561f59d45ffb4db5c8adab4f49bcc5b9b109a894e40c772dfafedc2b2fa8cc8
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

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:3d559bc8188bd91ca05fcd5915798e6194c6e5eaa5d9fe5fc52c9a73262bea49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143929709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc41e85e69d29cfcaf0664f071de3280933c76d2bef50af62dcc89dd9429fcd`
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

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:e19e495cdf71d3db037168b8c191e44bdb687a4bd72d96e72b4d451d61a2b5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a6ba70b6f2ddea9eafcdc1d5f0b07a5f0407636dcc869f70f1e316f3495403`

```dockerfile
```

-	Layers:
	-	`sha256:aff79abcfb64872e2682d75c637f4c1c0c70fcbaa0ac8e0d5567d31987dabc43`  
		Last Modified: Mon, 10 Nov 2025 21:07:40 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v6

```console
$ docker pull docker@sha256:3dd1b3434622289b26113052dd9c8063db1e1f6eac9fac63fd8622fe8c2c0e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138331609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8377e3b77449c9f356329ab39bec8e3139c423486fad8519c919ee0020e7dc90`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 00:44:47 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 18 Nov 2025 00:44:47 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 18 Nov 2025 00:44:47 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 18 Nov 2025 00:44:52 GMT
ENV DOCKER_VERSION=29.1.0-rc.1
# Tue, 18 Nov 2025 00:44:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 18 Nov 2025 00:44:52 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 18 Nov 2025 00:44:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 18 Nov 2025 00:44:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 18 Nov 2025 00:44:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 18 Nov 2025 00:44:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 18 Nov 2025 00:44:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:44:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 18 Nov 2025 00:44:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 18 Nov 2025 00:44:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:44:55 GMT
CMD ["sh"]
# Tue, 18 Nov 2025 01:12:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 18 Nov 2025 01:12:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 18 Nov 2025 01:12:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 18 Nov 2025 01:12:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 18 Nov 2025 01:12:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 18 Nov 2025 01:12:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 18 Nov 2025 01:12:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 01:12:15 GMT
VOLUME [/var/lib/docker]
# Tue, 18 Nov 2025 01:12:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 18 Nov 2025 01:12:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 18 Nov 2025 01:12:15 GMT
CMD []
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0f7826cb513c9a49b8db2290fb79e933a850876f7468f089777ead83903e33`  
		Last Modified: Tue, 18 Nov 2025 00:45:13 GMT  
		Size: 8.1 MB (8140533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c825ccc60c89146c70253d9ea5ae1a3a4da7dcec26ab4d38c6fa1d49bb004a30`  
		Last Modified: Tue, 18 Nov 2025 00:45:12 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d30d2890e6707c412e87fe29cffc595d9f2339d9a738695474664c51824878`  
		Last Modified: Tue, 18 Nov 2025 00:45:14 GMT  
		Size: 17.6 MB (17552166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe85c82c0a7bd33686e8756dee6111aca1b4d6413cac0a5c41f39d6b7736867`  
		Last Modified: Tue, 18 Nov 2025 00:45:14 GMT  
		Size: 21.5 MB (21476544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec78d38b9dbdde271f395be14b3626a467c8cfd23f2fe9d5f3ebe62953202671`  
		Last Modified: Tue, 18 Nov 2025 00:45:14 GMT  
		Size: 20.5 MB (20480372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926f9fef129d3c2bb8a7a3c70d997ab6d23382e1664848cc1c4edf08271c9294`  
		Last Modified: Tue, 18 Nov 2025 00:45:12 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4237ed7ba2487cac512bab75247451c633b0bca3247241c442523f15070e4a`  
		Last Modified: Tue, 18 Nov 2025 00:45:12 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c41b8d6f9323daaf5a195c19b2d2ace5297ae0c50866393e6b309089eb2fda`  
		Last Modified: Tue, 18 Nov 2025 00:45:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb5920376123f81bfb94d1b6573b38567e0d1b17fc16250d3b28d9ebb0ea277`  
		Last Modified: Tue, 18 Nov 2025 01:12:36 GMT  
		Size: 7.2 MB (7230310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6935fa4f09d2b29cebe25893bb495de8fa072bd5f9f99e33b3f4d792247638a`  
		Last Modified: Tue, 18 Nov 2025 01:12:35 GMT  
		Size: 89.9 KB (89948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2a53326301403a1f9d93e9cd8bc1cb9d7930648cfdbbbf4d066a81de73ba6`  
		Last Modified: Tue, 18 Nov 2025 01:12:35 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e534ec96c7afa799a23c6b02dd0cf82f25867362d3117ea42c90ed67a3fdcb`  
		Last Modified: Tue, 18 Nov 2025 01:12:42 GMT  
		Size: 59.8 MB (59849499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14c567de8a5db3f58d0a22a41a7cb4930240dc96abeec16b7aa12b63e9a7544`  
		Last Modified: Tue, 18 Nov 2025 01:12:35 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ff8e73c1c45950d87706080c46f1dc95d6a9291a4664c9e16dde4ecc068e01`  
		Last Modified: Tue, 18 Nov 2025 01:12:35 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:0cfba9db12ebd63977321dd4ec0db54b2851fdb4b78d192e6c9d5501b2fb5256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dece92ac22bc2cacccc9c0e4519d270baa492ff77b105677531c00a27cdd4387`

```dockerfile
```

-	Layers:
	-	`sha256:59448bff7481604af798b3eae4d09e79793e919daa83b7c6c61224af8bd56930`  
		Last Modified: Tue, 18 Nov 2025 03:10:32 GMT  
		Size: 34.2 KB (34235 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba0da83064cac4a208a28d49767e3eaefa7df971865bce94a031ab8308e1806b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136445256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e6537fc1c8af5e611508ac4ea7135496fb34359197d6c1866d18f1a9ac9a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 00:44:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 18 Nov 2025 00:44:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 18 Nov 2025 00:44:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 18 Nov 2025 00:44:44 GMT
ENV DOCKER_VERSION=29.1.0-rc.1
# Tue, 18 Nov 2025 00:44:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 18 Nov 2025 00:44:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 18 Nov 2025 00:44:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 18 Nov 2025 00:44:45 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 18 Nov 2025 00:44:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 18 Nov 2025 00:44:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 18 Nov 2025 00:44:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:44:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 18 Nov 2025 00:44:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 18 Nov 2025 00:44:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:44:46 GMT
CMD ["sh"]
# Tue, 18 Nov 2025 01:14:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 18 Nov 2025 01:14:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 18 Nov 2025 01:14:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 18 Nov 2025 01:14:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 18 Nov 2025 01:14:30 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 18 Nov 2025 01:14:30 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 18 Nov 2025 01:14:30 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 01:14:30 GMT
VOLUME [/var/lib/docker]
# Tue, 18 Nov 2025 01:14:30 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 18 Nov 2025 01:14:30 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 18 Nov 2025 01:14:30 GMT
CMD []
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb311f6c3c19d0df986f3087859e65e4b408c94b37e135ec581ef192d0e45bd`  
		Last Modified: Tue, 18 Nov 2025 00:45:07 GMT  
		Size: 7.5 MB (7461416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5065ca6c1730680a0f6010e99c12c99111869cd6f5346e2567c01d54bf6398b2`  
		Last Modified: Tue, 18 Nov 2025 00:45:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8af43877ad7e2742092e06ad4ef20cdd928a51639ae163e9cf2a3898e7aee`  
		Last Modified: Tue, 18 Nov 2025 00:45:08 GMT  
		Size: 17.5 MB (17542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601c0bc928eda7e33bc08fd2db1b773c227cb17b5a56b8f2e8ad85c110f0113d`  
		Last Modified: Tue, 18 Nov 2025 00:45:08 GMT  
		Size: 21.5 MB (21454917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58fcabbe1bb19a4b4e2e0eaf2c427f0945a436bff8b64c09a920b1393950dbf`  
		Last Modified: Tue, 18 Nov 2025 00:45:09 GMT  
		Size: 20.5 MB (20462767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f89aaaa85fc93353d5e2d60586fee6a217606c75e8b3aeea196a63bc3bfa87`  
		Last Modified: Tue, 18 Nov 2025 00:45:06 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75c92008a3bc8383e758847cb8bf92010dac96a607ee3bc7da4a89279c22872`  
		Last Modified: Tue, 18 Nov 2025 00:45:06 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157c528d11d8862ec333a6b03b098b4ba6c87a8fbf1ad4f7ab54437f7cbfe196`  
		Last Modified: Tue, 18 Nov 2025 00:45:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd1e409ce317a8488c2266769482eea5160842241af2f74b1929103b61562f3`  
		Last Modified: Tue, 18 Nov 2025 01:14:48 GMT  
		Size: 6.5 MB (6538227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7bf80a0d0fd19ca17371260cfcc81e8acb08a68fa84b8e16d76d1e9d13bd3a`  
		Last Modified: Tue, 18 Nov 2025 01:14:48 GMT  
		Size: 86.4 KB (86396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37c435ec0e64a9c05de9b8ba75b5838f9bca2bf4d5e7e58319d7f47fa4a021b`  
		Last Modified: Tue, 18 Nov 2025 01:14:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a1a852b3adc93d6c2c225816acd6c7dac317c96b1c61ca114ce9c725349e36`  
		Last Modified: Tue, 18 Nov 2025 01:14:52 GMT  
		Size: 59.7 MB (59669572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2654fc670670b427e75efccb2440d8679ac1e239ec3386f585bf62a3415b86a`  
		Last Modified: Tue, 18 Nov 2025 01:14:48 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fedb818fd91c2275ea86661e5032893c6c92be5c839d7891018c68476e1fac`  
		Last Modified: Tue, 18 Nov 2025 01:14:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:05d5132fe4548715877148bc8627730988d0de37902ef7a33665298e901773f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755c26fa7c097646223be8c39d68f66d5cb602051e4442266202da111c2d1a7`

```dockerfile
```

-	Layers:
	-	`sha256:eec81aef5536e38baf4b7ff35a9b8a30daada9d62ba327bbbd829beabbcdd693`  
		Last Modified: Tue, 18 Nov 2025 03:10:35 GMT  
		Size: 34.2 KB (34236 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:52629624a4b50ffca12579316ce8f816bc629291fe021fd2896bebf52fa63a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135866924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba49fab3e1f5b65f23a6574b7b65000c9522eef0030653b08f19fe9cd5b5369f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 18 Nov 2025 00:44:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 18 Nov 2025 00:44:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 18 Nov 2025 00:44:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 18 Nov 2025 00:44:54 GMT
ENV DOCKER_VERSION=29.1.0-rc.1
# Tue, 18 Nov 2025 00:44:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 18 Nov 2025 00:44:54 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 18 Nov 2025 00:44:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 18 Nov 2025 00:44:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.3
# Tue, 18 Nov 2025 00:44:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-x86_64'; 			sha256='dba9d98e1ba5bfe11d88c99b9bd32fc4a0624a30fafe68eea34d61a3e42fd372'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv6'; 			sha256='cea4d6b6de410d220426806ef67ce7fadb4b914029f49a66fb222d4525ac6871'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-armv7'; 			sha256='66aa2f460820b17aaa71e65b2c70e55eb27c11bdb9816169c322065a5b016d29'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-aarch64'; 			sha256='d26373b19e89160546d15407516cc59f453030d9bc5b43ba7faf16f7b4980137'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-ppc64le'; 			sha256='9be50cafe912442b27af48c44516b7ce2a65777ff121acf241dd5dba09d4f36c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-riscv64'; 			sha256='b52a2dcb0c221b5abd1d14729ed118aa24cf79012b5f2f992ddf6bc9c2e7f9fd'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.40.3/docker-compose-linux-s390x'; 			sha256='3caf6694c974d13a2754689ffb8f93bc29d084ee60fb7f9ebd4b682264dad9fe'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 18 Nov 2025 00:44:56 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 18 Nov 2025 00:44:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 00:44:56 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 18 Nov 2025 00:44:56 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 18 Nov 2025 00:44:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 00:44:56 GMT
CMD ["sh"]
# Tue, 18 Nov 2025 01:12:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 18 Nov 2025 01:12:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 18 Nov 2025 01:12:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 18 Nov 2025 01:12:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.1.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.1.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.1.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.1.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 18 Nov 2025 01:12:56 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 18 Nov 2025 01:12:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 18 Nov 2025 01:12:56 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 01:12:56 GMT
VOLUME [/var/lib/docker]
# Tue, 18 Nov 2025 01:12:56 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 18 Nov 2025 01:12:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 18 Nov 2025 01:12:56 GMT
CMD []
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb7fb87e1512ecb6a820dfc6c92b7db06ed9042ec9d2626043202408f465359`  
		Last Modified: Tue, 18 Nov 2025 00:45:12 GMT  
		Size: 8.3 MB (8257251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c1d6da1f85d76d91925dd0f9ddaeee4a99f831c1b5d780421ff91eced6801c`  
		Last Modified: Tue, 18 Nov 2025 00:45:12 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399b8465f007d4fa87359898304af23d506cb21620c3840507e130152361e10c`  
		Last Modified: Tue, 18 Nov 2025 00:45:13 GMT  
		Size: 17.3 MB (17325969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c071438df7653567506fba2481acebbc9e051e3f1bcd913abbae43c552e8ed`  
		Last Modified: Tue, 18 Nov 2025 00:45:12 GMT  
		Size: 20.6 MB (20645064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeb4f6f9ec17f5b79108650ffd26856e927dc20ad25e30c8a95edf3cc70a848`  
		Last Modified: Tue, 18 Nov 2025 00:45:13 GMT  
		Size: 19.9 MB (19869855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c47da8982ca6bbbcc70080313d0d0c79647ae92b26441ceceefe611ab2227`  
		Last Modified: Tue, 18 Nov 2025 00:45:11 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c7427fa61f6fe2582602e37d581ecf1f27d01509a1d80a15aba305697d5a9`  
		Last Modified: Tue, 18 Nov 2025 00:45:11 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eae4d02db04ce15454f6bac9c872a7588749805fa76fdecd66a99de92afa84`  
		Last Modified: Tue, 18 Nov 2025 00:45:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a6a317137e09b25feb16f6d6e687a3a234ede98b8695d2ffc13d31a99c27e9`  
		Last Modified: Tue, 18 Nov 2025 01:13:18 GMT  
		Size: 7.1 MB (7140802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f5fa4949f10b19b009f6f7e4aefcae2d0bc8215f4e064979e90f5ee74c516`  
		Last Modified: Tue, 18 Nov 2025 01:13:15 GMT  
		Size: 99.5 KB (99498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c15598be62a91f79364de7336a43a101de14c6e573fe76237147537e69ea1d`  
		Last Modified: Tue, 18 Nov 2025 01:13:15 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7647ad76c310b1e57115e432bbd5293c41c8351fb8f63e491bf6a32fa0c49587`  
		Last Modified: Tue, 18 Nov 2025 01:13:22 GMT  
		Size: 58.4 MB (58382265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe51ceadb034ea7bddb0d88dda76fceb46f929c2c0e702ce947e232a550bd5d`  
		Last Modified: Tue, 18 Nov 2025 01:13:16 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6af7a8c0707ff7a9057cf54857bdd93222d1bf26fb1cb376b50ec872e455466`  
		Last Modified: Tue, 18 Nov 2025 01:13:16 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc` - unknown; unknown

```console
$ docker pull docker@sha256:caad210f9d3146e0fdefc815c290ea6508ba83b5241022184aefd20829271a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78af19d94419fa65fd5d0ca591dba57c78d7fe3605c5e0653e89d88ca4d98ada`

```dockerfile
```

-	Layers:
	-	`sha256:f9497b6127d63d55fa42bb8ba7974dee600b62df3432c5dfb6f2231cd895b001`  
		Last Modified: Tue, 18 Nov 2025 03:10:38 GMT  
		Size: 34.3 KB (34284 bytes)  
		MIME: application/vnd.in-toto+json

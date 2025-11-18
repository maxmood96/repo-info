## `docker:29-rc-cli`

```console
$ docker pull docker@sha256:65fd37a238db464154846d28de02fb8233b3d57faeb3d14f5917ea454c173ef3
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

### `docker:29-rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:4a6a8a12a95e2b2d3bd1fbec92fc0c572d078258c90be60bc746245936aef5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74669093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521108df31796fa76f30b6719391ace012d7ab8bec845535135e7c603f51624d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:744569a91bb46b6316f0b1518f8375b1252369bc1183e327704df820597cf171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8ca9510d257880b190176014b06408fa5c2d4a24acf05d794f0bb17500d397`

```dockerfile
```

-	Layers:
	-	`sha256:07cf282b43a81b5900892c4d8c1c75feaaffd5738a6088b8197cf0104c8899dc`  
		Last Modified: Mon, 10 Nov 2025 21:08:03 GMT  
		Size: 37.9 KB (37868 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:a65682a1d4093642579c6e3b8cae1641441012f7ddd27e3294ea2eb1f2364b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71155851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b4991b0772fe6fa9d1d9084d54dfb4ac903b7313ae6af29d715ec8223a1f2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:e9fc5f6f86d20bace0c93f8168f3d41daa3e0361f2e1191960a4f1d180701cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55da0040363b4b4a486e57a62ecfb4c0bf207af97859858c73381bb78555a4ed`

```dockerfile
```

-	Layers:
	-	`sha256:08a32e3bd0e5094e46008ac222872a1a83c64011da8cdfe79797c3586a5c6bd8`  
		Last Modified: Tue, 18 Nov 2025 03:10:44 GMT  
		Size: 38.0 KB (38026 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:01ed5c25dc46494f5bb2430878b742e48d8f6e361dce96d99141628f4b486613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70145064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec55f65a32499adfa025b02cccd9d59013143949011f83f0dd831af7c2a68b7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8f8462de7e2ef642ae31d198fdbb526d8d12f4bca570f90393345057fa8ba5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e655cb3bff75fed4f535f4e9c9fb939f3eaec3abee00450fe76cd285d3006e93`

```dockerfile
```

-	Layers:
	-	`sha256:508bb1659ef931b397c0e37ebdd17dbdd6aead8f3c0ae4eca56132318db96123`  
		Last Modified: Tue, 18 Nov 2025 03:10:47 GMT  
		Size: 38.0 KB (38026 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9e7466099957d24f7bc38ba8d50dc3a90a5ce2f65a3fa0fb4f9b157367530ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70238361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4b22a952e7faee744bbce306db453fa9af897b6330f56080acba1ccef9f889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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

### `docker:29-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:111ec44e0694b6ef19107ca742e4bda88aa49bee800bb745821cf7854ffa28f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e8cd8474d198e9678e466b4f0a9687233367c0770931487049e9b3cfa06ad`

```dockerfile
```

-	Layers:
	-	`sha256:c3f97ea05ff0a1249a61ad183c47bd9378a5be0016b7efb092c1d08b26875800`  
		Last Modified: Tue, 18 Nov 2025 03:10:53 GMT  
		Size: 38.1 KB (38062 bytes)  
		MIME: application/vnd.in-toto+json
